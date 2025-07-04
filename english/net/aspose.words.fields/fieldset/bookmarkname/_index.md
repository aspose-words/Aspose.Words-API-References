---
title: FieldSet.BookmarkName
linktitle: BookmarkName
articleTitle: BookmarkName
second_title: Aspose.Words for .NET
description: Discover the FieldSet BookmarkName property to easily manage and customize your bookmarks. Enhance your application's navigation with this key feature!
type: docs
weight: 20
url: /net/aspose.words.fields/fieldset/bookmarkname/
---
## FieldSet.BookmarkName property

Gets or sets the name of the bookmark.

```csharp
public string BookmarkName { get; set; }
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

Assert.That(fieldSet.GetFieldCode(), Is.EqualTo(" SET  MyBookmark \"Hello world!\""));

// Refer to the bookmark by name in a REF field and display its contents.
FieldRef fieldRef = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
fieldRef.BookmarkName = "MyBookmark";
fieldRef.Update();

Assert.That(fieldRef.GetFieldCode(), Is.EqualTo(" REF  MyBookmark"));
Assert.That(fieldRef.Result, Is.EqualTo("Hello world!"));

doc.Save(ArtifactsDir + "Field.SET.REF.docx");
```

### See Also

* class [FieldSet](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
