/* $(function() {
    $("#city_form").validate({
        // Specify the validation rules
        rules: {
            state_id  : 	    {
                                    required: true                                     
                                },
            city_name   :   "required",
            status      :   {
                                required: true,
                                number: true
                            }
        },
    
        // Specify the validation error messages
        /*messages: {
            first_name          :   "Please enter First Name",
            last_name           :   "Please enter Last Name",
            contact_no          :   "Please enter Contact No.",
            email               :   "Please enter Email Address"
        },*/
    
/*    submitHandler: function(form) {
            form.submit();
        }
    });

}); */ 

function validate_form(){
    z=true;
    if($('#name').val()==''){
        $('#name_err').html('Please Enter Name');
        z=false;
    }
 
    if(z){
//         alert('dfkn');
        $('#cms_form').submit();
    }
}

function delete_retailers(id)
{
//    alert(id);
    if(id)
    {
        if(confirm('Are you sure, you want to delete this record'))
        {
            var token_value=$( "input[name='"+token_name+"']" ).val();
			
            $.ajax
            ({
                type: "POST",
                url: siteurl+'manage_retailers/delete',
                data: token_name+"="+token_value+"&id="+id,
                beforeSend: function(){
                    $(".overlay").show();
                },
                success: function(response)
                { 
//                    alert(response);
                    window.location.href=siteurl+'manage_retailers/list_items';
                }
            });
        }
    }
    else
    {
        alert('Please Select at least one Record');
    }
}
//==============Checked All and Unchecked all==============//
function checkAllRows()
{
    if($('#checkAllRows').is(':checked'))
    {
        $('.checkerDiv').each(function(){
            $('#'+this.id).prop('checked', true); // true
        });
    }
    else
    {
        $('.checkerDiv').each(function(){
            $('#'+this.id).prop('checked', false); // true
        });
    }
}
//==============Close Checked All and Unchecked all==============//
//==============Multiple delete==============//
$('#multidelete').click(function(){
    var deltechxbRow = [];
    $('[name="checkRow[]"]:checked').each(function(i){
        deltechxbRow[i] = $('#'+this.id).val();								 
    });
    if(deltechxbRow.length>=1)
    {
        if(confirm('Are you sure, you want to delete this record'))
        {
            var token_value=$( "input[name='"+token_name+"']" ).val();
            $.ajax
            ({
                type: "POST",
                url: siteurl+'mobile_app/manage_retailers/delete',
                data: token_name+"="+token_value+"&id="+deltechxbRow,
                beforeSend: function(){
                    $(".overlay").show();
                },
                success: function(response)
                { 
                    window.location.href=siteurl+'mobile_app/manage_retailers/list_items';
                }
            }); 
        }
    }
    else
    {
        alert("Sorry, Please Select at least one record!");
        return false;
    }       
})
//==============Close Multiple delete==============//

//===========Expoprt Excel Sheet===================//
function export_excel()
{
   var itemlist =[];
    $('[name="checkRow[]"]:checked').each(function(i){
            itemlist.push($(this).val());
    });
    if(itemlist.length>=1)
    {
        window.location.href=siteurl+'manage_retailers/export/?items='+itemlist;
        
        
    }
    else
    {
        alert("Sorry, Please Select at least one record!");
        return false;
    }
    
}
//===========Expoprt Excel Sheet===================//

//==============PDF================================//
function save_pdf()
{
    var itemlist =[];
    $('[name="checkRow[]"]:checked').each(function(i){
            itemlist.push($(this).val());
    });
    if(itemlist.length>=1)
    {
        window.location.href=siteurl+'manage_retailers/downloadpdf/?items='+itemlist;
        
        
    }
    else
    {
        alert("Sorry, Please Select at least one record!");
        return false;
    }
}
//=============Close PDF===========================//
//===============Return back on Listing============//
function return_backurl()
{
    window.location.href=siteurl+'manage_retailers/list_items';
}

$('#ip_based').change(function(){
    if($(this).val()=='1')
    {
        $('#ip_div').show();
    }else{
        $('#ip_div').hide();
    }
})

var num_row=1;
function addmoreIPAddress()
{
    ++num_row;
    var row='<div class="row" id="row_'+num_row+'"><div class="col-md-12"><div class="form-group"><label class="control-label col-md-2"> </label><div class="col-md-4"><input type="text" name="ip_address[]" id="ipaddress_'+num_row+'" class="form-control" lang="text[]"/><div style="color:red" id="error_ip_address'+num_row+'"></div></div><div class="col-md-4"><a class="btn btn-primary" id="add_more" onclick="addmoreIPAddress()"> <i class="fa fa-plus"></i>  Add More</a><a class="btn btn-default mini" href="javascript:void(0)" id="row_'+num_row+'" onclick="removeRow(this.id)"><i class="fa fa-trash"></i> Delete</a></div></div></div></div>';
	
    $('#ip_div').append(row);
	
}
function removeRow(id)
{
    $('#'+id).remove();
}
var edit_num_row= $('#ip_count').val();
function editmoreIPAddress(){
	
    ++edit_num_row;
    var row='<div class="row" id="row_'+edit_num_row+'"><div class="col-md-12"><div class="form-group"><label class="control-label col-md-2"> </label><div class="col-md-4"><input type="text" name="ip_address[]" id="ipaddress_'+edit_num_row+'" class="form-control" lang="text[]"/><div style="color:red" id="error_ip_address'+edit_num_row+'"></div></div><div class="col-md-4"><a class="btn btn-primary" id="add_more" onclick="addmoreIPAddress()"> <i class="fa fa-plus"></i>  Add More</a><a class="btn btn-default mini" href="javascript:void(0)" id="row_'+edit_num_row+'" onclick="removeRow(this.id)"><i class="fa fa-trash"></i> Delete</a></div></div></div></div>';
	
    $('#ip_div').append(row);
}
//===============Return back on Listing============//