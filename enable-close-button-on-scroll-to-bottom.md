## Enable modal close button on scroll to bottom
#### HTML
```html
<div class="modal fade scrollable-modal" id="modalId" tabindex="-1" role="dialog" aria-labelledby="exampleModalTextTitle" aria-hidden="true">
    <div class="modal-dialog modal-dialog-centered modal-lg" role="document">
        <div class="modal-content">
            <div class="modal-header">
                <h5 class="modal-title" id="exampleModalTextTitle">
                    TITLE
                </h5>
                <button type="button" class="close" data-dismiss="modal" aria-label="Close">
                    <span aria-hidden="true">&times;</span>
                </button>
            </div>
            <div class="modal-body scrollable-modal-body">
                text here...
            </div>
            <div class="modal-footer">
                <button type="button" 
                        class="btn btn-danger btn-active-on-scroll-bottom" 
                        data-dismiss="modal" 
                        disabled="disabled">Close</button>
            </div>
        </div>
    </div>
</div>
```

#### js
```js
/**
 * Enable close button on scroll to bottom
 */
function enableBtn(cssSelector){
    let $domObject = $(cssSelector);
    if($domObject){
        $domObject.prop('disabled', false);
    }
}

function disableBtn(cssSelector){
    let $domObject = $(cssSelector);
    if($domObject){
        $domObject.prop('disabled', true);
    }
}

function setScrollableDivScrollEvent(scrollableDivSelector, scrollToBottomTolerance, onScrolledToBottom){
    
    console.log("setScrollableDivScrollEvent()");

    let $scrollableDiv = $(scrollableDivSelector);
    if($scrollableDiv){

        $scrollableDiv.scroll(function(e) {
            let $scrollDiv = $(this);
            let visibleHeight = $scrollDiv.outerHeight();
            let contentScrollHeight = $scrollDiv[0].scrollHeight;
            let scrollTop = $scrollDiv.scrollTop();
            //console.log("visibleHeight => " + visibleHeight);
            //console.log("contentScrollHeight => " + contentScrollHeight);
            //console.log("scrollTop => " + scrollTop);

            let contentSeen = (visibleHeight + scrollTop);
            //console.log("contentSeen => " + contentSeen);
            
            let distanceToBottom = (contentScrollHeight - contentSeen);
            if(distanceToBottom <= scrollToBottomTolerance){
               onScrolledToBottom();
               return;
            }
        });
    }
}

function initModalCloseBtnActivation(scrollableModalSelector, srollableModalBodySelector, srollableModalCloseBtnSelector, scrollToBottomTolerance){
    console.log("initializing text modal close btn activation...");

    let $scrollableModal = $(scrollableModalSelector);
    
    // reset scrollbar to top
    $scrollableModal.on("shown.bs.modal", function(e){
        console.log("modal is shown");
        $(srollableModalBodySelector).scrollTop(0);
    });
    
    // close button activation
    setScrollableDivScrollEvent(srollableModalBodySelector, scrollToBottomTolerance, function(){
        console.log("srolled to bottom...");
        enableBtn(srollableModalCloseBtnSelector);
    });
    
    // disable close button when closed
    $scrollableModal.on("hide.bs.modal", function(e){
        console.log("modal is closed. disable btn");
        
        disableBtn(srollableModalCloseBtnSelector);
    });
}

$(function(e){
    let scrollableModalSelector = '.scrollable-modal';
    let srollableModalBodySelector = '.scrollable-modal-body';
    let srollableModalCloseBtnSelector = '.btn-active-on-scroll-bottom';
    let scrollToBottomTolerance = 1;
    initModalCloseBtnActivation(scrollableModalSelector, srollableModalBodySelector, srollableModalCloseBtnSelector, scrollToBottomTolerance);
});
```
