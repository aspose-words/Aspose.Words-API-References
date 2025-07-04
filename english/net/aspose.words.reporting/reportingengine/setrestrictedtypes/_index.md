---
title: ReportingEngine.SetRestrictedTypes
linktitle: SetRestrictedTypes
articleTitle: SetRestrictedTypes
second_title: Aspose.Words for .NET
description: Discover how the SetRestrictedTypes method in ReportingEngine enhances security by limiting member access in template syntax for optimized data reporting.
type: docs
weight: 80
url: /net/aspose.words.reporting/reportingengine/setrestrictedtypes/
---
## ReportingEngine.SetRestrictedTypes method

Specifies types, which members as well as which derived types' members should be inaccessible by the engine through template syntax.

```csharp
public static void SetRestrictedTypes(params Type[] types)
```

| Parameter | Type | Description |
| --- | --- | --- |
| types | Type[] | Types to be restricted. |

## Remarks

Restricted types should be set before the very first building of a report. After `BuildReport` is invoked, restricted types cannot be modified and an exception is thrown on attempt to do this. The best place to set restricted types is application startup.

Note that a big amount of restricted types may affect performance, so it is better to restrict only those types, access to which members is really sensitive.

Throws ArgumentException in the following cases:

- *types* is null.

- One of *types* items is `null`.

- One of *types* items represents an invisible type, i.e. a non-public type or a public nested type which has a non-public outer type.

- One of *types* items represents an array type.

- *types* contain duplicate entries.

## Examples

Shows how to deny access to members of types considered insecure.

```csharp
Document doc =
    DocumentHelper.CreateSimpleDocument(
        "<<var [typeVar = \"\".GetType().BaseType]>><<[typeVar]>>");

// Note, that you can't set restricted types during or after building a report.
ReportingEngine.SetRestrictedTypes(typeof(System.Type));
// We set "AllowMissingMembers" option to avoid exceptions during building a report.
ReportingEngine engine = new ReportingEngine() { Options = ReportBuildOptions.AllowMissingMembers };
engine.BuildReport(doc, new object());

// We get an empty string because we can't access the GetType() method.
Assert.That(doc.GetText().Trim(), Is.EqualTo(string.Empty));
```

### See Also

* class [ReportingEngine](../)
* namespace [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* assembly [Aspose.Words](../../../)
