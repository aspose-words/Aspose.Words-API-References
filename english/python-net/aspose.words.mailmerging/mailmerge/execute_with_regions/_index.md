---
title: MailMerge.execute_with_regions method
linktitle: execute_with_regions method
articleTitle: execute_with_regions method
second_title: Aspose.Words for Python
description: "aspose.words.mailmerging.MailMerge.execute_with_regions method"
type: docs
weight: 190
url: /python-net/aspose.words.mailmerging/mailmerge/execute_with_regions/
---

## execute_with_regions(data_source) {#imailmergedatasource}

Performs a mail merge from a custom data source with mail merge regions.


```python
def execute_with_regions(self, data_source: aspose.words.mailmerging.IMailMergeDataSource):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| data_source | [IMailMergeDataSource](../../imailmergedatasource/) | An object that implements the custom mail merge data source interface. |

### Remarks

Use this method to fill mail merge fields in the document with values from
any custom data source such as an XML file or collections of business objects. You need to write your
own class that implements the [IMailMergeDataSource](../../imailmergedatasource/) interface.

You can use this method only when [FieldOptions.is_bidi_text_supported_on_update](../../../aspose.words.fields/fieldoptions/is_bidi_text_supported_on_update/) is ``False``,
that is you do not need Right-To-Left language (such as Arabic or Hebrew) compatibility.




## execute_with_regions(data_source_root) {#imailmergedatasourceroot}

Performs a mail merge from a custom data source with mail merge regions.


```python
def execute_with_regions(self, data_source_root: aspose.words.mailmerging.IMailMergeDataSourceRoot):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| data_source_root | [IMailMergeDataSourceRoot](../../imailmergedatasourceroot/) | An object that implements the custom mail merge data source root interface. |

### Remarks

Use this method to fill mail merge fields in the document with values from
any custom data source such as an XML file or collections of business objects. You need to write your own classes
that implement the [IMailMergeDataSourceRoot](../../imailmergedatasourceroot/) and [IMailMergeDataSource](../../imailmergedatasource/) interfaces.

You can use this method only when [FieldOptions.is_bidi_text_supported_on_update](../../../aspose.words.fields/fieldoptions/is_bidi_text_supported_on_update/) is ``False``,
that is you do not need Right-To-Left language (such as Arabic or Hebrew) compatibility.




## Examples

Shows how to use mail merge regions to execute a nested mail merge.

```python
def test_custom_data_source(self):

    doc = aw.Document()
    builder = aw.DocumentBuilder(doc)

    # Normally, MERGEFIELDs contain the name of a column of a mail merge data source.
    # Instead, we can use "TableStart:" and "TableEnd:" prefixes to begin/end a mail merge region.
    # Each region will belong to a table with a name that matches the string immediately after the prefix's colon.
    builder.insert_field(" MERGEFIELD TableStart:Customers")

    # These MERGEFIELDs are inside the mail merge region of the "Customers" table.
    # When we execute the mail merge, this field will receive data from rows in a data source named "Customers".
    builder.write("Full name:\t")
    builder.insert_field(" MERGEFIELD FullName ")
    builder.write("\nAddress:\t")
    builder.insert_field(" MERGEFIELD Address ")
    builder.write("\nOrders:\n")

    # Create a second mail merge region inside the outer region for a data source named "Orders".
    # The "Orders" data entries have a many-to-one relationship with the "Customers" data source.
    builder.insert_field(" MERGEFIELD TableStart:Orders")

    builder.write("\tItem name:\t")
    builder.insert_field(" MERGEFIELD Name ")
    builder.write("\n\tQuantity:\t")
    builder.insert_field(" MERGEFIELD Quantity ")
    builder.insert_paragraph()

    builder.insert_field(" MERGEFIELD TableEnd:Orders")
    builder.insert_field(" MERGEFIELD TableEnd:Customers")

    # Create related data with names that match those of our mail merge regions.
    customers = []
    customers.append(ExMailMergeCustomNested.Customer("Thomas Hardy", "120 Hanover Sq., London"))
    customers.append(ExMailMergeCustomNested.Customer("Paolo Accorti", "Via Monte Bianco 34, Torino"))

    customers[0].orders.append(ExMailMergeCustomNested.Order("Rugby World Cup Cap", 2))
    customers[0].orders.append(ExMailMergeCustomNested.Order("Rugby World Cup Ball", 1))
    customers[1].orders.append(ExMailMergeCustomNested.Order("Rugby World Cup Guide", 1))

    # To mail merge from your data source, we must wrap it into an object that implements the IMailMergeDataSource interface.
    customers_data_source = ExMailMergeCustomNested.CustomerMailMergeDataSource(customers)

    doc.mail_merge.execute_with_regions(customers_data_source)

    doc.save(ARTIFACTS_DIR + "NestedMailMergeCustom.custom_data_source.docx")

class Customer:
    """An example of a "data entity" class in your application."""

    def __init__(self, full_name: str, address: str):

        self.full_name = full_name
        self.address = address
        self.orders = [] # type: List[Order]

class Order:
    """An example of a child "data entity" class in your application."""

    def __init__(self, name: str, quantity: int):

        self.name = name
        self.quantity = quantity

class CustomerMailMergeDataSource(aw.mailmerging.IMailMergeDataSource):
    """A custom mail merge data source that you implement to allow Aspose.Words
    to mail merge data from your Customer objects into Microsoft Word documents."""

    def __init__(self, customers):

        self.customers = customers

        # When we initialize the data source, its position must be before the first record.
        self.record_index = -1

    @property
    def table_name(self):
        """The name of the data source. Used by Aspose.Words only when executing mail merge with repeatable regions."""

        return "Customers"

    def get_value(self, field_name: str):
        """Aspose.Words calls this method to get a value for every data field."""

        if field_name == "FullName":
            return self.customers[self.record_index].full_name

        if field_name == "Address":
            return self.customers[self.record_index].address

        if field_name == "Order":
            return self.customers[self.record_index].orders

        # Return "None" to the Aspose.Words mail merge engine to signify
        # that we could not find a field with this name.
        return None

    def move_next(self):
        """A standard implementation for moving to a next record in a collection."""

        if not self.is_eof:
            self.record_index += 1

        return not self.is_eof

    def get_child_data_source(self, table_name: str):

        # Get the child data source, whose name matches the mail merge region that uses its columns.
        if table_name == "Orders":
            return ExMailMergeCustomNested.OrderMailMergeDataSource(self.ustomers[self.record_index].orders)

        return None

    @property
    def is_eof(self) -> bool:

        return self.record_index >= len(self.customers)

class OrderMailMergeDataSource(aw.mailmerging.IMailMergeDataSource):

    def __init__(self, orders):

        self.orders = orders

        # When we initialize the data source, its position must be before the first record.
        self.record_index = -1

    @property
    def table_name(self) -> str:
        """The name of the data source. Used by Aspose.Words only when executing mail merge with repeatable regions."""

        return "Orders"

    def get_value(self, field_name: str):
        """Aspose.Words calls this method to get a value for every data field."""

        if field_name == "Name":
            return self.orders[self.record_index].name

        if field_name == "Quantity":
            return self.orders[self.record_index].quantity

        # Return "None" to the Aspose.Words mail merge engine to signify
        # that we could not find a field with this name.
        return None

    def move_next(self) -> bool:
        """A standard implementation for moving to a next record in a collection."""

        if not self.is_eof:
            self.record_index += 1

        return not self.is_eof

    def get_child_data_source(self, table_name: str) -> aw.mailmerging.IMailMergeDataSource:
        """Return None because we do not have any child elements for this sort of object."""

        return None

    @property
    def is_eof(self) -> bool:

        return self.record_index >= len(self.orders)
```

Performs mail merge from a custom data source with master-detail data.

```python
def test_custom_data_source_root(self):

    # Create a document with two mail merge regions named "Washington" and "Seattle".
    mail_merge_regions = ["Vancouver", "Seattle"]
    doc = ExMailMergeCustom.create_source_document_with_mail_merge_regions(mail_merge_regions)

    # Create two data sources for the mail merge.
    employees_washington_branch = [] # type: List[Employee]
    employees_washington_branch.add(ExMailMergeCustom.Employee("John Doe", "Sales"))
    employees_washington_branch.add(ExMailMergeCustom.Employee("Jane Doe", "Management"))

    employees_seattle_branch = [] # type: List[Employee]
    employees_seattle_branch.add(ExMailMergeCustom.Employee("John Cardholder", "Management"))
    employees_seattle_branch.add(ExMailMergeCustom.Employee("Joe Bloggs", "Sales"))

    # Register our data sources by name in a data source root.
    # If we are about to use this data source root in a mail merge with regions,
    # each source's registered name must match the name of an existing mail merge region in the mail merge source document.
    source_root = ExMailMergeCustom.DataSourceRoot()
    source_root.register_source(mail_merge_regions[0], ExMailMergeCustom.EmployeeListMailMergeSource(employees_washington_branch))
    source_root.register_source(mail_merge_regions[1], ExMailMergeCustom.EmployeeListMailMergeSource(employees_seattle_branch))

    # Since we have consecutive mail merge regions, we would normally have to perform two mail merges.
    # However, one mail merge source with a data root can fill in multiple regions
    # if the root contains tables with corresponding names/column names.
    doc.mail_merge.execute_with_regions(source_root)

    doc.save(ARTIFACTS_DIR + "MailMergeCustom.custom_data_source_root.docx")

@staticmethod
def create_source_document_with_mail_merge_regions(regions: List[str]) -> aw.Document:
    """Create a document that contains consecutive mail merge regions, with names designated by the input array,
    for a data table of employees."""

    doc = aw.Document()
    builder = aw.DocumentBuilder(doc)

    for region in regions:
        builder.writeln("\n" + region + " branch: ")
        builder.insert_field(" MERGEFIELD TableStart:" + region)
        builder.insert_field(" MERGEFIELD FullName")
        builder.write(", ")
        builder.insert_field(" MERGEFIELD Department")
        builder.insert_field(" MERGEFIELD TableEnd:" + region)

    return doc

class Employee:
    """An example of a "data entity" class in your application."""

    def __init__(self, full_name: str, department: str):

        self.full_name = full_name
        self.department = department

class DataSourceRoot(aw.mailmerging.IMailMergeDataSourceRoot):
    """Data source root that can be passed directly into a mail merge which can register and contain many child data sources.
    These sources must all implement IMailMergeDataSource, and are registered and differentiated by a name
    which corresponds to a mail merge region that will read the respective data."""

    def __init__(self):
        self.sources: Dict[str, ExMailMergeCustom.EmployeeListMailMergeSource] = {}

    def get_data_source(self, table_name: str) -> aw.mailmerging.IMailMergeDataSource:

        source = self.sources[table_name]
        source.reset()
        return self.sources[table_name]

    def register_source(self, source_name: str, source: ExMailMergeCustom.EmployeeListMailMergeSource):

        self.sources.add(source_name, source)

class EmployeeListMailMergeSource(aw.mailmerging.IMailMergeDataSource):
    """Custom mail merge data source."""

    def __init__(self, employees: List[ExMailMergeCustom.Employee]):

        self.employees = employees
        self.record_index = -1

    def move_next(self) -> bool:
        """A standard implementation for moving to a next record in a collection."""

        if not self.is_eof:
            self.record_index += 1

        return not self.is_eof

    @property
    def is_eof(self) -> bool:

        return self.record_index >= len(self.employees)

    def test_reset(self):

        self.record_index = -1

    @property
    def table_name(self) -> str:
        """The name of the data source. Used by Aspose.Words only when executing mail merge with repeatable regions."""

        return "Employees"

    def get_value(self, field_name: str) -> str:
        """Aspose.Words calls this method to get a value for every data field."""

        if field_name == "FullName":
            return self.employees[self.record_index].full_name

        if field_name == "Department":
            return self.employees[self.record_index].department

        # Return "None" to the Aspose.Words mail merge engine to signify
        # that we could not find a field with this name.
        return None

    def get_child_data_source(self, table_name: str) -> aw.mailmerging.IMailMergeDataSource:
        """Child data sources are for nested mail merges."""

        raise NotImplementedError()
```

## See Also

* module [aspose.words.mailmerging](../../)
* class [MailMerge](../)

