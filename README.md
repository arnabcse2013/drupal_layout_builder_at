# drupal_layout_builder_at
The purpose of this project is to build a translated node with different languages and having an inline_entity_form-complex nested blocks.

**Issue:**
1. Create a node in EN and go to layout builder. Add new components having nested blocks and save.
2. Click on translate and create a FR node. Check the checkbox 'Copy blocks into translation'.
3. It creates a new FR language and copies only the parent blocks and thus skips the nested blocks having type 'inline entity form-complex'.

**Solution:**
Create a patch that will copy the parent as well as the nested blocks. The nessted blocks should have translated nodes for different languages.

**Drupal Community:**
Thanks to the drupal community :)
There is a patch available for the issue: https://www.drupal.org/project/layout_builder_at/issues/3098245
But the above patch always creates a new or translated node for any language for a nested block also regardless, thus following the layout_builder_at architecture.

**Updated Patch:**
I have updated the same patch and refactored the function to create a translation of the nested block, thus following Drupal's way of working.

**Modules Required:**
1. Inline Entity Form - https://www.drupal.org/project/inline_entity_form
2. Layout Builder At - https://www.drupal.org/project/layout_builder_at

**Cheers to All. Have a beautiful day :-D**
