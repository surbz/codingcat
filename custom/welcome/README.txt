1.Reverting a feature programatically 

function mymodule_update_X() {
  features_revert(array('module' => array('component'))); 
  // or features_revert();
  //or features_revert(array('my_features_pack' => array('fe_block_settings')));
}


for mutiple features
<?php
/**
 * Implements hook_update_N().
 *
 * Revert all content-related features, necessary for using correct view mode.
 */
function example_update_7005() {
  sdl_features_revert(array('feature_about', 'feature_awards', 'feature_events', 'feature_news', 'feature_people', 'feature_projects', 'feature_frontend'));
}
?>


2.Drupal functions used in validations while form submits like - is_numeric()

3.Hooks use cases (Read about top drupal hooks and how can i use them)
hook_init - to set global vars on non-cached pages,
hook_boot - used on cached pages to set global vars

4.Final Exam Points





