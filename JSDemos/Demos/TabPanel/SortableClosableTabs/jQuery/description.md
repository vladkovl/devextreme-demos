This demo illustrates how you can allow end-users to reorder, add, and remove tabs within the DevExtreme [TabPanel](/Documentation/ApiReference/UI_Components/dxTabPanel/) component.     

**Reorder tabs**       

Wrap the TabPanel into the [Sortable](/Documentation/ApiReference/UI_Components/dxSortable/) component and set the following properties as needed:

- [filter](/Documentation/ApiReference/UI_Components/dxSortable/Configuration/#filter)         
Specify a CSS selector to indicate draggable items. This demo sets filter to `.dx-tab`.

- [itemOrientation](/Documentation/ApiReference/UI_Components/dxSortable/Configuration/#itemOrientation)           
Set this property to *"horizontal"*. When a user drags a tab, remaining items move left and right to designate the drop target.

- [onReorder](/Documentation/ApiReference/UI_Components/dxSortable/Configuration/#onReorder)       
Implement this handler to synchronize the [dataSource](/Documentation/ApiReference/UI_Components/dxTabPanel/Configuration/#dataSource) with reordered tabs.

- [moveItemOnDrop](/Documentation/ApiReference/UI_Components/dxSortable/Configuration/#moveItemOnDrop)
Set this property to **true** to update markup after a tab is dropped.

**Add or remove tabs**      

This demo adds and removes tabs in the following two functions:

- `addButtonHandler` - a click handler for the *"Add Tab"* button.
- `closeButtonHandler` - a click handler for a tab's Close icon. The demo uses the [itemTitleTemplate](/Documentation/ApiReference/UI_Components/dxTabPanel/Configuration/#itemTitleTemplate) property to display this icon.

Both handlers modify the TabPanel's [dataSource](/Documentation/ApiReference/UI_Components/dxTabPanel/Configuration/#dataSource).