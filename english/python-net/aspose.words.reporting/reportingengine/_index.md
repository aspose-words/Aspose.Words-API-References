---
title: ReportingEngine class
second_title: Aspose.Words for Python via .NET API Reference
description: "Provides routines to populate template documents with data and a set of settings to control these routines."
type: docs
weight: 80
url: /python-net/aspose.words.reporting/reportingengine/
---

## ReportingEngine class

Provides routines to populate template documents with data and a set of settings to control these routines.


### Constructors
| Name | Description |
| --- | --- |
| [ReportingEngine()](./__init__/#default) | Initializes a new instance of this class. |

### Properties

| Name | Description |
| --- | --- |
| [known_types](./known_types/) | Gets an unordered set (i.e. a collection of unique items) containing System.Type objects  which fully or partially qualified names can be used within report templates processed by this engine instance to invoke the corresponding types' static members, perform type casts, etc. |
| [options](./options/) | Gets or sets a set of flags controlling behavior of this [ReportingEngine](./) instance  while building a report. |
| [use_reflection_optimization](./use_reflection_optimization/) | Gets or sets a value indicating whether invocations of custom type members performed via reflection API are  optimized using dynamic class generation or not. The default value is true. |

### Methods

| Name | Description |
| --- | --- |
|[ build_report(document, data_source)](./build_report/#document_object) | Populates the specified template document with data from the specified source making it a ready report. |
|[ build_report(document, data_source, data_source_name)](./build_report/#document_object_str) | Populates the specified template document with data from the specified source making it a ready report. |
|[ build_report(document, data_sources, data_source_names)](./build_report/#document_objectlist_strlist) | Populates the specified template document with data from the specified sources making it a ready report. |

### See Also

* module [aspose.words.reporting](../)

