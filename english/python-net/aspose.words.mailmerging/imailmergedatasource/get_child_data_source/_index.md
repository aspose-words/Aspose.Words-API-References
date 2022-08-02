---
title: get_child_data_source method
second_title: Aspose.Words for Python via .NET API Reference
description: "The Aspose.Words mail merge engine invokes this method when it encounters a beginning of a nested mail merge region."
type: docs
weight: 20
url: /python-net/aspose.words.mailmerging/imailmergedatasource/get_child_data_source/
---

## get_child_data_source(table_name) {#str}

The Aspose.Words mail merge engine invokes this method when it encounters a beginning of a nested mail merge region.


```python
def get_child_data_source(self, table_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| table_name | str |  |

When the Aspose.Words mail merge engines populates a mail merge region with data and encounters the beginning of a nested
mail merge region in the form of MERGEFIELD TableStart:TableName, it invokes [IMailMergeDataSource.get_child_data_source()](./#str) on the current
data source object. Your implementation needs to return a new data source object that will provide access to the child
records of the current parent record. Aspose.Words will use the returned data source to populate the nested mail merge region.


Below are the rules that the implementation of [IMailMergeDataSource.get_child_data_source()](./#str) must follow.


If the table that is represented by this data source object has a related child (detail) table with the specified name,
then your implementation needs to return a new [IMailMergeDataSource](../) object that will provide access
to the child records of the current record.

An example of this is Orders / OrderDetails relationship. Let's assume that the current [IMailMergeDataSource](../) object
represents the Orders table and it has a current order record. Next, Aspose.Words encounters "MERGEFIELD TableStart:OrderDetails"
in the document and invokes [IMailMergeDataSource.get_child_data_source()](./#str). You need to create and return a [IMailMergeDataSource](../)
object that will allow Aspose.Words to access the OrderDetails record for the current order.


If this data source object does not have a relation to the table with the specified name, then you need to return
a [IMailMergeDataSource](../) object that will provide access to all records of the specified table.


If a table with the specified name does not exist, your implementation should return ``null``.





### Returns

A data source object that will provide access to the data records of the specified table.


### Examples

Shows how to execute a mail merge with a data source in the form of a custom object.

```python
def test_custom_data_source(self):

    doc = aw.Document()
    builder = aw.DocumentBuilder(doc)
    builder.insert_field(" MERGEFIELD FullName ")
    builder.insert_paragraph()
    builder.insert_field(" MERGEFIELD Address ")

    customers = [] # type: List[Customer]
    customers.add(Customer("Thomas Hardy", "120 Hanover Sq., London"))
    customers.add(Customer("Paolo Accorti", "Via Monte Bianco 34, Torino"))

    # To use a custom object as a data source, it must implement the IMailMergeDataSource interface.
    data_source = ExMailMergeCustom.CustomerMailMergeDataSource(customers)

    doc.mail_merge.execute(data_source)

    doc.save(ARTIFACTS_DIR + "MailMergeCustom.custom_data_source.docx")

class Customer:
    """An example of a "data entity" class in your application."""

    def __init__(self, full_name: str, address: str):

        self.full_name = full_name
        self.address = address

class CustomerMailMergeDataSource(aw.mailmerging.IMailMergeDataSource):
    """A custom mail merge data source that you implement to allow Aspose.Words
    to mail merge data from your Customer objects into Microsoft Word documents."""

    def __init__(self, customers: 'List[ExMailMergeCustom.Customer]'):

        self.customers = customers

        # When we initialize the data source, its position must be before the first record.
        self.record_index = -1

    @property
    def table_name(self) -> str:
        """The name of the data source. Used by Aspose.Words only when executing mail merge with repeatable regions."""

        return "Customer"

    def get_value(self, field_name: str) -> str:
        """Aspose.Words calls this method to get a value for every data field."""

        if field_name == "FullName":
            return self.customers[self.record_index].full_name

        if field_name ==  "Address":
            return self.customers[self.record_index].address

        # Return "None" to the Aspose.Words mail merge engine to signify
        # that we could not find a field with this name.
        return None

    def move_next(self) -> bool:
        """A standard implementation for moving to a next record in a collection."""

        if not self.is_eof:
            self.record_index += 1

        return not self.is_eof

    def get_child_data_source(self, table_name: str):

        return None

    @property
    def is_eof(self) -> bool:

        return self.record_index >= len(self.customers)
```

### See Also

* module [aspose.words.mailmerging](../../)
* class [IMailMergeDataSource](../)

