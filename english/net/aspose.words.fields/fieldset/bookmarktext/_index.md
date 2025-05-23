---
title: FieldSet.BookmarkText
linktitle: BookmarkText
articleTitle: BookmarkText
second_title: Aspose.Words for .NET
description: Discover how to easily manage the FieldSet BookmarkText property to customize and enhance your bookmarks for better organization and accessibility.
type: docs
weight: 30
url: /net/aspose.words.fields/fieldset/bookmarktext/
---
## FieldSet.BookmarkText property

Gets or sets the new text of the bookmark.

```csharp
public string BookmarkText { get; set; }
```

## Examples

Shows how to create bookmarked text with a SET field, and then display it in the document using a REF field.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Name bookmarked text with a SET field. 
// This field refers to the "bookmark" not a bookmark structure that appears within the text, but a named variable.
FieldSet fieldSet = (FieldSet)builder.InsertField(FieldType.FieldSet, false);
fieldSet.BookmarkName = "MyBookmark";
fieldSet.BookmarkText = "Hello world!";
fieldSet.Update();

Assert.AreEqual(" SET  MyBookmark \"Hello world!\"", fieldSet.GetFieldCode());

// Refer to the bookmark by name in a REF field and display its contents.
FieldRef fieldRef = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
fieldRef.BookmarkName = "MyBookmark";
fieldRef.Update();

Assert.AreEqual(" REF  MyBookmark", fieldRef.GetFieldCode());
Assert.AreEqual("Hello world!", fieldRef.Result);

doc.Save(ArtifactsDir + "Field.SET.REF.docx");
```

### See Also

* class [FieldSet](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
