/v1/projects/{project_id}/iou/vms/{vm_id}/adapters/{adapter_number:\d+}/ports/{port_number:\d+}/start_capture
----------------------------------------------------------------------------------------------------------------------

.. contents::

POST /v1/projects/**{project_id}**/iou/vms/**{vm_id}**/adapters/**{adapter_number:\d+}**/ports/**{port_number:\d+}**/start_capture
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Start a packet capture on a IOU VM instance

Parameters
**********
- **adapter_number**: Adapter to start a packet capture
- **port_number**: Port on the adapter
- **project_id**: UUID for the project
- **vm_id**: UUID for the instance

Response status codes
**********************
- **200**: Capture started
- **400**: Invalid request
- **404**: Instance doesn't exist
- **409**: VM not started

Input
*******
.. raw:: html

    <table>
    <tr>                 <th>Name</th>                 <th>Mandatory</th>                 <th>Type</th>                 <th>Description</th>                 </tr>
    <tr><td>capture_file_name</td>                    <td>&#10004;</td>                     <td>string</td>                     <td>Capture file name</td>                     </tr>
    <tr><td>data_link_type</td>                    <td>&#10004;</td>                     <td>string</td>                     <td>PCAP data link type</td>                     </tr>
    </table>

Sample session
***************


.. literalinclude:: ../../examples/post_projectsprojectidiouvmsvmidadaptersadapternumberdportsportnumberdstartcapture.txt

