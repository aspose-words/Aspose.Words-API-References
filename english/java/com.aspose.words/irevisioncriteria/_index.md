---
title: IRevisionCriteria
linktitle: IRevisionCriteria
second_title: Aspose.Words for Java
description: Implement this interface if you want to control when certain Revision should be accepted/rejected or not by the RevisionCollection.acceptcom.aspose.words.IRevisionCriteria/ RevisionCollection.rejectcom.aspose.words.IRevisionCriteria methods in Java.
type: docs
weight: 714
url: /java/com.aspose.words/irevisioncriteria/
---
```
public interface IRevisionCriteria
```

Implement this interface if you want to control when certain [Revision](../../com.aspose.words/revision/) should be accepted/rejected or not by the [RevisionCollection.accept(com.aspose.words.IRevisionCriteria)](../../com.aspose.words/revisioncollection/\#accept-com.aspose.words.IRevisionCriteria)/ [RevisionCollection.reject(com.aspose.words.IRevisionCriteria)](../../com.aspose.words/revisioncollection/\#reject-com.aspose.words.IRevisionCriteria) methods.
## Methods

| Method | Description |
| --- | --- |
| [isMatch(Revision revision)](#isMatch-com.aspose.words.Revision) | Checks whether or not specified  revision  matches criteria. |
### isMatch(Revision revision) {#isMatch-com.aspose.words.Revision}
```
public abstract boolean isMatch(Revision revision)
```


Checks whether or not specified  revision  matches criteria.

 **Remarks:** 

The method implementation should not accept/reject the revision or modify it in any way due to unexpected results.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| revision | [Revision](../../com.aspose.words/revision/) | The [Revision](../../com.aspose.words/revision/) instance to match criteria. |

**Returns:**
boolean -  True  if the  revision  matches criteria, otherwise  False .
