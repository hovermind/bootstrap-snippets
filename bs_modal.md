## Create Modal
```
<div class="modal fade" id="my-modal" tabindex="-1" role="dialog" aria-labelledby="" aria-hidden="true">
	<div class="modal-dialog" role="document modal-content">
		<div class="modal-content">
			<div class="modal-header">

				<div style='text-align: right; float: right'>
					<button type="button" class="close" data-dismiss="modal" aria-label="Close">&times;</button>
				</div>

				<h2 class="modal-title">
					<strong>My Modal Title</strong>
				</h2>

			</div>

			<div class="modal-body">
				<div class="panel panel-default">
					<div class="panel-body">

						<div role="alert" class="alert alert-danger">
							<strong>Warning!</strong>
							My Warning Message
						</div>

						<div class="form-group">

							<label class="control-label">User Id</label>
							<input id="user-id" name="user-id" type="number" placeholder="Enter Id" class="form-control">

						</div>
						
						<div class="form-group">

							<label class="control-label">User Name</label>
							<input id="user-name" name="user-name" type="text" placeholder="Enter User Name" class="form-control" />

						</div>
						
						<div class="form-group">

							<label class="control-label">Gender</label>
							<select id="gender-select" name="gender-select" class="form-control">
								<option value="m" text="Male"></option>
								<option value="f" text="Female"></option>
							</select>

						</div>

						<!--/* feedback message to user */-->
						<div role="alert" class="alert feedback-success alert-dismissable" id="feedback_div">
							<div style='text-align: left'>
								<div style='text-align: right; float: right'>
									<button data-dismiss="alert" class='close alert-close' aria-label="close" aria-hidden='true' tabindex='-1'>&times;</button>
								</div>
								<strong id="feedback_message">Feedback Message</strong>
							</div>
						</div>

						<div class="form-group" style="float: right;">
							<button type="button" class="btn btn-success" id="btn-creat-user">Create</button>
							<button type="button" class="btn btn-danger" data-dismiss="modal" id="btn-close">Close</button>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</div>
```


## Show Modal
```
<button id="btn-my-modal" type="button" class="btn btn-success" data-toggle="modal" data-target="#my-modal">Create User</button>
```
or programmatically
```
let $myModal = $('#my-modal');
$myModal.modal('show');
//$myModal.modal('hide');
```


## Modal Events
```
let $myModal = $('#my-modal');

$myModal.on('show.bs.modal', function(e) {

	//e.preventDefault();
	//console.log("show.bs.modal");
	
	// show feedback
	$('#feedback_message').html('this is feedback message to user');
	$('#feedback_div').show();

	let clickedBtnId = e.relatedTarget.id;
	// ...
});

$myModal.on('hidden.bs.modal', function(e) {

	//e.preventDefault();
	//console.log("hidden.bs.modal");

	//hide feedback
	$('#feedback_message').html('');
	$('#feedback_div').hide();
	
});

// other events
//$myModal.on('shown.bs.modal', function(e) {});
//$myModal.on('hide.bs.modal', function(e) {});
```
