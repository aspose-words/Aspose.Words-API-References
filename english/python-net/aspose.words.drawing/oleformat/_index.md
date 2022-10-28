---
title: OleFormat class
second_title: Aspose.Words for Python via .NET API Reference
description: "Provides access to the data of an OLE object or ActiveX control"
type: docs
weight: 220
url: /python-net/aspose.words.drawing/oleformat/
---

## OleFormat class

Provides access to the data of an OLE object or ActiveX control.
To learn more, visit the [Working with Ole Objects](https://docs.aspose.com/words/net/working-with-ole-objects-and-online-video/) documentation article.




Use the [Shape.ole_format](../shape/ole_format/) property to access the data of an OLE object.
You do not create instances of the [OleFormat](./) class directly.




### Properties

| Name | Description |
| --- | --- |
| [auto_update](./auto_update/) | Specifies whether the link to the OLE object is automatically updated or not in Microsoft Word. |
| [clsid](./clsid/) | Gets the CLSID of the OLE object. |
| [icon_caption](./icon_caption/) | Gets icon caption of OLE object. In case of OLE object is not embedded as icon or caption couldn't be retrieved returns empty string. |
| [is_link](./is_link/) | Returns ``True`` if the OLE object is linked (when [OleFormat.source_full_name](./source_full_name/) is specified). |
| [is_locked](./is_locked/) | Specifies whether the link to the OLE object is locked from updates. |
| [ole_control](./ole_control/) | Gets [OleFormat.ole_control](./ole_control/) objects if this OLE object is an ActiveX control. Otherwise this property is ``None``. |
| [ole_icon](./ole_icon/) | Gets the draw aspect of the OLE object. When ``True``, the OLE object is displayed as an icon.  When ``False``, the OLE object is displayed as content. |
| [ole_package](./ole_package/) | Provide access to [OlePackage](../olepackage/) if OLE object is an OLE Package.  Returns ``None`` otherwise. |
| [prog_id](./prog_id/) | Gets or sets the ProgID of the OLE object. |
| [source_full_name](./source_full_name/) | Gets or sets the path and name of the source file for the linked OLE object. |
| [source_item](./source_item/) | Gets or sets a string that is used to identify the portion of the source file that is being linked. |
| [suggested_extension](./suggested_extension/) | Gets the file extension suggested for the current embedded object if you want to save it into a file. |
| [suggested_file_name](./suggested_file_name/) | Gets the file name suggested for the current embedded object if you want to save it into a file. |

### Methods

| Name | Description |
| --- | --- |
|[ get_ole_entry(ole_entry_name)](./get_ole_entry/#str) | Gets OLE object data entry. |
|[ get_raw_data()](./get_raw_data/#default) | Gets OLE object raw data. |
|[ save(stream)](./save/#bytesio) | Saves the data of the embedded object into the specified stream. |
|[ save(file_name)](./save/#str) | Saves the data of the embedded object into a file with the specified name. |

### Examples

Shows how to extract embedded OLE objects into files.

```python
doc = aw.Document(MY_DIR + "OLE spreadsheet.docm")
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()

# The OLE object in the first shape is a Microsoft Excel spreadsheet.
ole_format = shape.ole_format

self.assertEqual("Excel.Sheet.12", ole_format.prog_id)

# Our object is neither auto updating nor locked from updates.
self.assertFalse(ole_format.auto_update)
self.assertEqual(False, ole_format.is_locked)

# If we plan on saving the OLE object to a file in the local file system,
# we can use the "suggested_extension" property to determine which file extension to apply to the file.
self.assertEqual(".xlsx", ole_format.suggested_extension)

# Below are two ways of saving an OLE object to a file in the local file system.
# 1 -  Save it via a stream:
with open(ARTIFACTS_DIR + "OLE spreadsheet extracted via stream" + ole_format.suggested_extension, "wb") as file:
    ole_format.save(file)

# 2 -  Save it directly to a filename:
ole_format.save(ARTIFACTS_DIR + "OLE spreadsheet saved directly" + ole_format.suggested_extension)
```

### See Also

* module [aspose.words.drawing](../)
* property [Shape.ole_format](../shape/ole_format/)

