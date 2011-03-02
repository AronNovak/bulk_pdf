= Bulk PDF

- Installation
Download the required modules, for dompdf, you need to download the library as well from http://code.google.com/p/dompdf/. Go to admin/build/modules and enable Bulk PDF module.

- Usage
Create a view with Views Bulk Operations style, choose Generate bulk PDF as an action.
Choose which content-type you want to use as a model, edit the content-type and tick "Use as a Bulk PDF model", usually you want to create a separate content-type for this purpose.
Create the first model node, you can use the tokens appearing on the node edit form, those will be filled using the selected nodes from VBO.
Go to the views, select the needed nodes, then the model and the module generates you the needed PDF. The module only takes care of the body field of the model node.

- Tips and tricks
You can use <p style="page-break-after:always" /> in the bottom of the model node body, to make the selected node appear on separate pages.




