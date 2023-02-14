## Remove Menu Page

```
// REMOVE MENU PAGE
function remove_menus(){
  
  remove_menu_page( 'index.php' );                  //Dashboard
  remove_menu_page( 'edit.php' );                   //Posts
  remove_menu_page( 'upload.php' );                 //Media
  remove_menu_page( 'edit.php?post_type=page' );    //Pages
  remove_menu_page( 'edit-comments.php' );          //Comments
  remove_menu_page( 'themes.php' );                 //Appearance
  remove_menu_page( 'plugins.php' );                //Plugins
  remove_menu_page( 'users.php' );                  //Users
  remove_menu_page( 'tools.php' );                  //Tools
  remove_menu_page( 'options-general.php' );        //Settings  
}
add_action( 'admin_menu', 'remove_menus' );
```
## Remove Submenu Page
```
// REMOVE SUBMENU PAGE

function remove_submenus() {
	remove_submenu_page( 'themes.php', 'widgets.php' );
	remove_submenu_page( 'users.php' , 'profile.php' ); 
	remove_submenu_page( 'themes.php', 'theme-editor.php'); //editor
}
add_action( 'admin_menu', 'remove_submenus' );
```

## References

[remove_menu_page](https://developer.wordpress.org/reference/functions/remove_menu_page/)

[remove_submenu_page](https://developer.wordpress.org/reference/functions/remove_submenu_page/)
