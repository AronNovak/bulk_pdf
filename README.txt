= Bulk PDF

- Installation
Download the required modules, for dompdf, you need to download the library as well from http://code.google.com/p/dompdf/. Go to admin/build/modules and enable Bulk PDF module.

- Usage
Create a view with Views Bulk Operations style, choose Generate bulk PDF as an action.
Choose which content-type you want to use as a model, edit the content-type and tick "Use as a Bulk PDF model", usually you want to create a separate content-type for this purpose.
Create the first model node, you can use the tokens appearing on the node edit form, those will be filled using the selected nodes from VBO.
Go to the views, select the needed nodes, then the model and the module generates you the needed PDF. The module only takes care of the body field of the model node.
The module generates a pdf per 100 data (VBO selected) node.
For example if you select 150 nodes via VBO, you get 2 PDF files, if you select 50, you get only one. See the tips and tricks part for performance considerations.

- Tips and tricks
You can use <p style="page-break-after:always" /> in the bottom of the model node body, to make the selected node appear on separate pages.
If you want to generate very complex pages for 100s of nodes, you likely need to set the PHP 'memory_limit' to a high value (like 256M or more..), also the same for max_execution_time, let's allow several minutes for dompdf to finish.

