# Connections---Deploy-Widget-to-all-users

DISCLAIMER:
<b>If you run this code, you should ALWAYS do a backup of the Homepage database first!<br></b>
<br>
IBM Connections provides Widget developers with the option to "open by default". Which should mean that everyone should get the widget pushed out into the Homepage app, right?..... Wrong!<br>
It turns out, this is only true when it comes to new users who has never logged into Connections before.<br><br>
That´s why I created these two TDI Assembly Lines. One for pushing out the Widget to "My Page" and to the right-hand side column on "Updates", and one Assembly Line to delete the widget again.<br><br>
The Homepage table is hard to get a grip on regarding understanding how it is all put together. But I think I found the correct tables for this. It seems so, after I tested it out on my own server.<br><br>

The two Assembly Files needs to be imported into your own custom TDI solutions directory through "File - Import" and then select "General - File System".<br><br>
<b>PREREQS:</b><br>
Go through all of the Connectors to insert your database server name, username and password on the "Connection" tab..<br>
I did not bother to insert this in a properties file, sorry about that. :-)<br><br>
And also, you need to find your widget id, and put this into the "setAttributes" - widget_id in both of the assembly lines.<br>
The Widget_id can be found in the HOMEPAGE.WIDGET table. Column 3, contains the name of your installed widget. Column 1 contains the Widget ID, which is the one you need to insert in the Assembly Lines.<br>
