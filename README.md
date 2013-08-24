this is a little plugin with jQuery to render json data in html table.

there are two stlye in this plugin: 1.normal table;2.extended table.

extended table is a table with static part and dynamic part , dynamic part will scroll left and right with more data to show

usage :
	
	normal table : $(selector).jtable(data,fields);

	extended table : $(selector).jextable(options);

index is a demo to check.

struct in fields:

"theadtr", "theadth", "theadtd", "tbodytr", "tbodytd", "tfoottr", "tfoottd" is some speciall field to render special data which is not showing in table

field has three keys:

field = {
	field , key of the data to render;
	name , table head in thead;
	format , customerize format in table cell,this will warp into <td></td>/<th></th> to compele the cell,
}	

in format you can use @+key (key in data) to make you special field with mutily data to show 

special field:
	
	theadtr : to render in thead in tr format, like <tr id=@id>
	theadth : to render in thead in th format, like <th data-field=@field>
	tbodytr : to render in tbody in tr format, like <tr id=@id>
	tbodytd : to render in tbody in td format, like <td field=@field>