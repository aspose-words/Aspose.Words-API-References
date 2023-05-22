---
title: IMailMergeDataSource.move_next method
linktitle: move_next method
articleTitle: move_next method
second_title: Aspose.Words for Python
description: "IMailMergeDataSource.move_next method. Advances to the next record in the data source."
type: docs
weight: 40
url: /python-net/aspose.words.mailmerging/imailmergedatasource/move_next/
---

## move_next() {#default}

Advances to the next record in the data source.


```python
def move_next(self):
    ...
```

### Returns

``True`` if moved to next record successfully; ``False`` if reached end of the data source.


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

