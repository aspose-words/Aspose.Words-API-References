---
title: MailMergeRegionInfo
second_title: Aspose.Words for Java API Reference
description: Contains information about a mail merge region.
type: docs
weight: 385
url: /java/com.aspose.words/mailmergeregioninfo/
---

**Inheritance:**
java.lang.Object
```
public class MailMergeRegionInfo
```

Contains information about a mail merge region.

To learn more, visit the **Mail Merge and Reporting** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [getParentRegion()](#getParentRegion--) | Returns parent region info (null for top-level region). |
| [getRegions()](#getRegions--) | Returns a list of child regions. |
| [getFields()](#getFields--) | Returns a list of child fields. |
| [getName()](#getName--) | Returns the name of region. |
| [getStartField()](#getStartField--) | Returns a start field for the region. |
| [getEndField()](#getEndField--) | Returns an end field for the region. |
| [getLevel()](#getLevel--) | Returns the nesting level for the region. |
### getParentRegion() {#getParentRegion--}
```
public MailMergeRegionInfo getParentRegion()
```


Returns parent region info (null for top-level region).

**Returns:**
[MailMergeRegionInfo](../../com.aspose.words/mailmergeregioninfo) - Parent region info (null for top-level region).
### getRegions() {#getRegions--}
```
public ArrayList getRegions()
```


Returns a list of child regions.

**Returns:**
java.util.ArrayList - A list of child regions.
### getFields() {#getFields--}
```
public ArrayList getFields()
```


Returns a list of child fields.

**Returns:**
java.util.ArrayList - A list of child fields.
### getName() {#getName--}
```
public String getName()
```


Returns the name of region.

**Returns:**
java.lang.String - The name of region.
### getStartField() {#getStartField--}
```
public FieldMergeField getStartField()
```


Returns a start field for the region.

**Returns:**
[FieldMergeField](../../com.aspose.words/fieldmergefield) - A start field for the region.
### getEndField() {#getEndField--}
```
public FieldMergeField getEndField()
```


Returns an end field for the region.

**Returns:**
[FieldMergeField](../../com.aspose.words/fieldmergefield) - An end field for the region.
### getLevel() {#getLevel--}
```
public int getLevel()
```


Returns the nesting level for the region.

**Returns:**
int - The nesting level for the region.
