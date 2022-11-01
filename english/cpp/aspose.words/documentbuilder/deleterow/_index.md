---
title: DeleteRow
second_title: Aspose.Words for C++ API Reference
description: Deletes a row from a table.
type: docs
weight: 14
url: /cpp/aspose.words/documentbuilder/deleterow/
---
## DocumentBuilder.DeleteRow method


Deletes a row from a table.

```cpp
System::SharedPtr<Aspose::Words::Tables::Row> Aspose::Words::DocumentBuilder::DeleteRow(int32_t tableIndex, int32_t rowIndex)
```


| Parameter | Type | Description |
| --- | --- | --- |
| tableIndex | int32_t | The index of the table. |
| rowIndex | int32_t | The index of the row in the table. |

### ReturnValue


The row node that was just removed.

If the cursor is inside the row that is being deleted, the cursor is moved out to the next row or to the next paragraph after the table.

If you delete a row from a table that contains only one row, the whole table is deleted.

For the index parameters, when index is greater than or equal to 0, it specifies an index from the beginning with 0 being the first element. When index is less than 0, it specified an index from the end with -1 being the last element.

## Examples




Shows how to delete a row from a table. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, cell 2.");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Row 2, cell 1.");
builder->InsertCell();
builder->Write(u"Row 2, cell 2.");
builder->EndTable();

ASSERT_EQ(2, table->get_Rows()->get_Count());

// Delete the first row of the first table in the document.
builder->DeleteRow(0, 0);

ASSERT_EQ(1, table->get_Rows()->get_Count());
ASSERT_EQ(u"Row 2, cell 1.\aRow 2, cell 2.\a\a", table->GetText().Trim());
```

