---
title: ComparerContext Class
linktitle: ComparerContext
articleTitle: ComparerContext
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aspose.Words LowCode ComparerContext-Klasse für einen effizienten Dokumentenvergleich und verbessern Sie Ihren Workflow durch nahtlose Integration und leistungsstarke Funktionen.
type: docs
weight: 4220
url: /de/net/aspose.words.lowcode/comparercontext/
---
## ComparerContext class

Dokumentvergleichskontext

```csharp
public class ComparerContext : ProcessorContext
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [ComparerContext](comparercontext/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [AcceptRevisions](../../aspose.words.lowcode/comparercontext/acceptrevisions/) { get; set; } | Gibt an, ob Revisionen in den Dokumenten vor dem Vergleich akzeptiert werden sollen. Wenn die verglichenen Dokumente Revisionen enthalten und dieses Flag auf „false“ gesetzt ist, lehnt der Prozessor Revisionen ab. Der Standardwert ist`WAHR` . |
| [Author](../../aspose.words.lowcode/comparercontext/author/) { get; set; } | Der Autor, der den während des Dokumentvergleichs erstellten Revisionen zugewiesen werden soll. |
| [CompareOptions](../../aspose.words.lowcode/comparercontext/compareoptions/) { get; } | Beim Vergleichen von Dokumenten verwendete Optionen. |
| [DateTime](../../aspose.words.lowcode/comparercontext/datetime/) { get; set; } | Das Datum und die Uhrzeit, die den während des Dokumentvergleichs erstellten Revisionen zugewiesen wurden. |
| [FontSettings](../../aspose.words.lowcode/processorcontext/fontsettings/) { get; set; } | Vom Prozessor verwendete Schriftarteinstellungen. |
| [LayoutOptions](../../aspose.words.lowcode/processorcontext/layoutoptions/) { get; } | Vom Prozessor verwendete Dokumentlayoutoptionen. |
| [WarningCallback](../../aspose.words.lowcode/processorcontext/warningcallback/) { get; set; } | Vom Prozessor verwendeter Warn-Callback. |

## Beispiele

Zeigt, wie man Dokumente einfach anhand des Kontexts vergleicht.

```csharp
// Es gibt mehrere Möglichkeiten, Dokumente zu vergleichen:
string firstDoc = MyDir + "Table column bookmarks.docx";
string secondDoc = MyDir + "Table column bookmarks.doc";

ComparerContext comparerContext = new ComparerContext();
comparerContext.CompareOptions.IgnoreCaseChanges = true;
comparerContext.Author = "Author";
comparerContext.DateTime = new DateTime();

Comparer.Create(comparerContext)
    .From(firstDoc)
    .From(secondDoc)
    .To(ArtifactsDir + "LowCode.CompareContextDocuments.docx")
    .Execute();
```

Zeigt, wie Dokumente aus dem Stream mithilfe des Kontexts verglichen werden.

```csharp
// Es gibt mehrere Möglichkeiten, Dokumente aus dem Stream zu vergleichen:
using (FileStream firstStreamIn = new FileStream(MyDir + "Table column bookmarks.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Table column bookmarks.doc", FileMode.Open, FileAccess.Read))
    {
        ComparerContext comparerContext = new ComparerContext();
        comparerContext.CompareOptions.IgnoreCaseChanges = true;
        comparerContext.Author = "Author";
        comparerContext.DateTime = new DateTime();

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.CompareContextStreamDocuments.docx", FileMode.Create, FileAccess.ReadWrite))
            Comparer.Create(comparerContext)
                .From(firstStreamIn)
                .From(secondStreamIn)
                .To(streamOut, SaveFormat.Docx)
                .Execute();
    }
}
```

### Siehe auch

* class [ProcessorContext](../processorcontext/)
* namensraum [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../)
