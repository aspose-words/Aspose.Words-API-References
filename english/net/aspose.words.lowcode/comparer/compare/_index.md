---
title: Comparer.Compare
linktitle: Compare
articleTitle: Compare
second_title: Aspose.Words for .NET
description: Comparer Compare method. Compares two documents and saves the differences to the specified output file producing changes as a number of edit and format revisions in C#.
type: docs
weight: 10
url: /net/aspose.words.lowcode/comparer/compare/
---
## Compare(*string, string, string, string, DateTime*) {#compare_4}

Compares two documents and saves the differences to the specified output file, producing changes as a number of edit and format revisions.

```csharp
public static void Compare(string v1, string v2, string outputFileName, string author, 
    DateTime dateTime)
```

| Parameter | Type | Description |
| --- | --- | --- |
| v1 | String | The original document. |
| v2 | String | The modified document. |
| outputFileName | String | The output file name. |
| author | String | Initials of the author to use for revisions. |
| dateTime | DateTime | The date and time to use for revisions. |

## Examples

Shows how to simple compare documents.

```csharp
// There is a several ways to compare documents:
string firstDoc = MyDir + "Table column bookmarks.docx";
string secondDoc = MyDir + "Table column bookmarks.doc";

Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.1.docx", "Author", new DateTime());
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.2.docx", SaveFormat.Docx, "Author", new DateTime());
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.3.docx", "Author", new DateTime(), new CompareOptions() { IgnoreCaseChanges = true });
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.4.docx", SaveFormat.Docx, "Author", new DateTime(), new CompareOptions() { IgnoreCaseChanges = true });
```

### See Also

* class [Comparer](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## Compare(*string, string, string, [SaveFormat](../../../aspose.words/saveformat/), string, DateTime*) {#compare_2}

Compares two documents and saves the differences to the specified output file in the provided save format, producing changes as a number of edit and format revisions.

```csharp
public static void Compare(string v1, string v2, string outputFileName, SaveFormat saveFormat, 
    string author, DateTime dateTime)
```

| Parameter | Type | Description |
| --- | --- | --- |
| v1 | String | The original document. |
| v2 | String | The modified document. |
| outputFileName | String | The output file name. |
| saveFormat | SaveFormat | The output's save format. |
| author | String | Initials of the author to use for revisions. |
| dateTime | DateTime | The date and time to use for revisions. |

## Examples

Shows how to simple compare documents.

```csharp
// There is a several ways to compare documents:
string firstDoc = MyDir + "Table column bookmarks.docx";
string secondDoc = MyDir + "Table column bookmarks.doc";

Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.1.docx", "Author", new DateTime());
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.2.docx", SaveFormat.Docx, "Author", new DateTime());
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.3.docx", "Author", new DateTime(), new CompareOptions() { IgnoreCaseChanges = true });
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.4.docx", SaveFormat.Docx, "Author", new DateTime(), new CompareOptions() { IgnoreCaseChanges = true });
```

### See Also

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Comparer](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## Compare(*string, string, string, string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare_5}

Compares two documents with additional options and saves the differences to the specified output file, producing changes as a number of edit and format revisions.

```csharp
public static void Compare(string v1, string v2, string outputFileName, string author, 
    DateTime dateTime, CompareOptions compareOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| v1 | String | The original document. |
| v2 | String | The modified document. |
| outputFileName | String | The output file name. |
| author | String | Initials of the author to use for revisions. |
| dateTime | DateTime | The date and time to use for revisions. |
| compareOptions | CompareOptions | Document comparison options. |

## Examples

Shows how to simple compare documents.

```csharp
// There is a several ways to compare documents:
string firstDoc = MyDir + "Table column bookmarks.docx";
string secondDoc = MyDir + "Table column bookmarks.doc";

Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.1.docx", "Author", new DateTime());
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.2.docx", SaveFormat.Docx, "Author", new DateTime());
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.3.docx", "Author", new DateTime(), new CompareOptions() { IgnoreCaseChanges = true });
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.4.docx", SaveFormat.Docx, "Author", new DateTime(), new CompareOptions() { IgnoreCaseChanges = true });
```

### See Also

* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## Compare(*string, string, string, [SaveFormat](../../../aspose.words/saveformat/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare_3}

Compares two documents with additional options and saves the differences to the specified output file in the provided save format, producing changes as a number of edit and format revisions.

```csharp
public static void Compare(string v1, string v2, string outputFileName, SaveFormat saveFormat, 
    string author, DateTime dateTime, CompareOptions compareOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| v1 | String | The original document. |
| v2 | String | The modified document. |
| outputFileName | String | The output file name. |
| saveFormat | SaveFormat | The output's save format. |
| author | String | Initials of the author to use for revisions. |
| dateTime | DateTime | The date and time to use for revisions. |
| compareOptions | CompareOptions | Document comparison options. |

## Examples

Shows how to simple compare documents.

```csharp
// There is a several ways to compare documents:
string firstDoc = MyDir + "Table column bookmarks.docx";
string secondDoc = MyDir + "Table column bookmarks.doc";

Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.1.docx", "Author", new DateTime());
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.2.docx", SaveFormat.Docx, "Author", new DateTime());
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.3.docx", "Author", new DateTime(), new CompareOptions() { IgnoreCaseChanges = true });
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.4.docx", SaveFormat.Docx, "Author", new DateTime(), new CompareOptions() { IgnoreCaseChanges = true });
```

### See Also

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## Compare(*Stream, Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), string, DateTime*) {#compare}

Compares two documents loaded from streams and saves the differences to the provided output stream in the specified save format, producing changes as a number of edit and format revisions.

```csharp
public static void Compare(Stream v1, Stream v2, Stream outputStream, SaveFormat saveFormat, 
    string author, DateTime dateTime)
```

| Parameter | Type | Description |
| --- | --- | --- |
| v1 | Stream | The original document. |
| v2 | Stream | The modified document. |
| outputStream | Stream | The output stream. |
| saveFormat | SaveFormat | The output's save format. |
| author | String | Initials of the author to use for revisions. |
| dateTime | DateTime | The date and time to use for revisions. |

## Examples

Shows how to compare documents from the stream.

```csharp
// There is a several ways to compare documents from the stream:
using (FileStream firstStreamIn = new FileStream(MyDir + "Table column bookmarks.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Table column bookmarks.doc", FileMode.Open, FileAccess.Read))
    {
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.CompareStreamDocuments.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Comparer.Compare(firstStreamIn, secondStreamIn, streamOut, SaveFormat.Docx, "Author", new DateTime());

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.CompareStreamDocuments.2.docx", FileMode.Create, FileAccess.ReadWrite))
            Comparer.Compare(firstStreamIn, secondStreamIn, streamOut, SaveFormat.Docx, "Author", new DateTime(), new CompareOptions() { IgnoreCaseChanges = true });
    }
}
```

### See Also

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Comparer](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## Compare(*Stream, Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare_1}

Compares two documents loaded from streams with additional options and saves the differences to the provided output stream in the specified save format, producing changes as a number of edit and format revisions.

```csharp
public static void Compare(Stream v1, Stream v2, Stream outputStream, SaveFormat saveFormat, 
    string author, DateTime dateTime, CompareOptions compareOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| v1 | Stream | The original document. |
| v2 | Stream | The modified document. |
| outputStream | Stream | The output stream. |
| saveFormat | SaveFormat | The output's save format. |
| author | String | Initials of the author to use for revisions. |
| dateTime | DateTime | The date and time to use for revisions. |
| compareOptions | CompareOptions | Document comparison options. |

## Examples

Shows how to compare documents from the stream.

```csharp
// There is a several ways to compare documents from the stream:
using (FileStream firstStreamIn = new FileStream(MyDir + "Table column bookmarks.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Table column bookmarks.doc", FileMode.Open, FileAccess.Read))
    {
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.CompareStreamDocuments.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Comparer.Compare(firstStreamIn, secondStreamIn, streamOut, SaveFormat.Docx, "Author", new DateTime());

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.CompareStreamDocuments.2.docx", FileMode.Create, FileAccess.ReadWrite))
            Comparer.Compare(firstStreamIn, secondStreamIn, streamOut, SaveFormat.Docx, "Author", new DateTime(), new CompareOptions() { IgnoreCaseChanges = true });
    }
}
```

### See Also

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)
