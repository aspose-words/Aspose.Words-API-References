---
title: ReportingEngine.GetRestrictedTypes
linktitle: GetRestrictedTypes
articleTitle: GetRestrictedTypes
second_title: Aspose.Words for .NET
description: Discover the ReportingEngine GetRestrictedTypes method, which identifies inaccessible member types and derived types for enhanced template syntax control.
type: docs
weight: 90
url: /net/aspose.words.reporting/reportingengine/getrestrictedtypes/
---
## ReportingEngine.GetRestrictedTypes method

Returns types, which members as well as which derived types' members should be inaccessible by the engine through template syntax.

```csharp
public static Type[] GetRestrictedTypes()
```

### Return Value

Types, which members as well as which derived types' members should be inaccessible by the engine through template syntax.

## Remarks

The returned array contains items previously set using [`SetRestrictedTypes`](../setrestrictedtypes/).

Changing items of the returned array has no effect on restricted types. To change restricted types, use [`SetRestrictedTypes`](../setrestrictedtypes/) instead.

### See Also

* class [ReportingEngine](../)
* namespace [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assembly [Aspose.Words](../../../)
