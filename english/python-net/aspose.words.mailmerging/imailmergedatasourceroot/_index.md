---
title: IMailMergeDataSourceRoot class
second_title: Aspose.Words for Python via .NET API Reference
description: "Implement this interface to allow mail merge from a custom data source with master-detail data."
type: docs
weight: 60
url: /python-net/aspose.words.mailmerging/imailmergedatasourceroot/
---

## IMailMergeDataSourceRoot class

Implement this interface to allow mail merge from a custom data source with master-detail data.


### Methods

| Name | Description |
| --- | --- |
|[ get_data_source(table_name)](./get_data_source/#str) | The Aspose.Words mail merge engine invokes this method when it encounters a beginning of a top-level mail merge region. |

### Examples

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

### See Also

* module [aspose.words.mailmerging](../)

