---
title: WarningInfoCollection class
second_title: Aspose.Words for Python via .NET API Reference
description: "Represents a typed collection of [WarningInfo](../warninginfo/) objects"
type: docs
weight: 1300
url: /python-net/aspose.words/warninginfocollection/
---

## WarningInfoCollection class

Represents a typed collection of [WarningInfo](../warninginfo/) objects.
To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/net/programming-with-documents/) documentation article.




You can use this collection object as the simplest form of [IWarningCallback](../iwarningcallback/) implementation to gather 
all warnings that Aspose.Words generates during a load or save operation. Create an instance of this class and assign it 
to the [LoadOptions.warning_callback](../../aspose.words.loading/loadoptions/warning_callback/) or [DocumentBase.warning_callback](../documentbase/warning_callback/) property.




**Interfaces:** [IWarningCallback](../iwarningcallback/)

### Constructors
| Name | Description |
| --- | --- |
| [WarningInfoCollection()](./__init__/#default) | The default constructor. |

### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Gets an item at the specified index. |

### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Gets the number of elements contained in the collection. |

### Methods

| Name | Description |
| --- | --- |
|[ clear()](./clear/#default) | Removes all elements from the collection. |
|[ warning(info)](./warning/#warninginfo) | Implements the [IWarningCallback](../iwarningcallback/) interface. Adds a warning to this collection. |

### See Also

* module [aspose.words](../)
* class [IWarningCallback](../iwarningcallback/)
* class [WarningInfo](../warninginfo/)

