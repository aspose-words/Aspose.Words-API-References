---
title: SmartTag Class
linktitle: SmartTag
articleTitle: SmartTag
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Markup.SmartTag, die die Dokumentbearbeitung verbessert, indem sie Smart Tags um Inline-Elemente wie Bilder und Felder identifiziert.
type: docs
weight: 4740
url: /de/net/aspose.words.markup/smarttag/
---
## SmartTag class

Dieses Element gibt das Vorhandensein eines Smarttags um eine oder mehrere Inline-Strukturen (Läufe, Bilder, Felder usw.) innerhalb eines Absatzes an.

Um mehr zu erfahren, besuchen Sie die[Strukturierte Dokument-Tags oder Inhaltssteuerung](https://docs.aspose.com/words/net/working-with-content-control-sdt/) Dokumentationsartikel.

```csharp
public class SmartTag : CompositeNode
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [SmartTag](smarttag/)(*[DocumentBase](../../aspose.words/documentbase/)*) | Initialisiert eine neue Instanz des`SmartTag` Klasse. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words/compositenode/count/) { get; } | Ruft die Anzahl der unmittelbar untergeordneten Elemente dieses Knotens ab. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ruft das Dokument ab, zu dem dieser Knoten gehört. |
| [Element](../../aspose.words.markup/smarttag/element/) { get; set; } | Gibt den Namen des Smarttags innerhalb des Dokuments an. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Ruft das erste untergeordnete Element des Knotens ab. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Rückgaben`WAHR` wenn dieser Knoten untergeordnete Knoten hat. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Rückgaben`WAHR` da dieser Knoten untergeordnete Knoten haben kann. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Ruft das letzte untergeordnete Element des Knotens ab. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| override [NodeType](../../aspose.words.markup/smarttag/nodetype/) { get; } | RückgabenSmartTag . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ruft den unmittelbar übergeordneten Knoten dieses Knotens ab. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar vorausgeht. |
| [Properties](../../aspose.words.markup/smarttag/properties/) { get; } | Eine Sammlung der Smarttag-Eigenschaften. |
| [Range](../../aspose.words/node/range/) { get; } | Gibt einen[`Range`](../../aspose.words/range/)Objekt, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist. |
| [Uri](../../aspose.words.markup/smarttag/uri/) { get; set; } | Gibt die Namespace-URI des Smarttags an. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Accept](../../aspose.words.markup/smarttag/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Nimmt einen Besucher auf. |
| override [AcceptEnd](../../aspose.words.markup/smarttag/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Akzeptiert einen Besucher für den Besuch des Endes des SmartTag. |
| override [AcceptStart](../../aspose.words.markup/smarttag/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Akzeptiert einen Besucher für den Besuch des Starts des SmartTags. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Fügt den angegebenen Knoten am Ende der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Erstellt ein Duplikat des Knotens. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Erstellt einen Navigator, der zum Durchlaufen und Lesen von Knoten verwendet werden kann. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Ruft den ersten Vorfahren des angegebenen[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Ruft den ersten Vorgänger des angegebenen Objekttyps ab. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | Gibt einen N-ten untergeordneten Knoten zurück, der dem angegebenen Typ entspricht. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Gibt eine Live-Sammlung von untergeordneten Knoten zurück, die dem angegebenen Typ entsprechen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bietet Unterstützung für die Iteration des For-Each-Stils über die untergeordneten Knoten dieses Knotens. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Ruft den Text dieses Knotens und aller seiner untergeordneten Knoten ab. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | Gibt den Index des angegebenen untergeordneten Knotens im untergeordneten Knoten-Array zurück. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../../aspose.words/node/)*) | Fügt den angegebenen Knoten unmittelbar nach dem angegebenen Referenzknoten ein. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../../aspose.words/node/)*) | Fügt den angegebenen Knoten unmittelbar vor dem angegebenen Referenzknoten ein. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Ruft den nächsten Knoten gemäß dem Pre-Order-Tree-Traversal-Algorithmus ab. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | Fügt den angegebenen Knoten am Anfang der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Ruft den vorherigen Knoten gemäß dem Pre-Order-Tree-Traversal-Algorithmus ab. |
| [Remove](../../aspose.words/node/remove/)() | Entfernt sich selbst vom übergeordneten Element. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Entfernt alle untergeordneten Knoten des aktuellen Knotens. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Entfernt den angegebenen untergeordneten Knoten. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Entfernt alle`SmartTag` Nachkommenknoten des aktuellen Knotens. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Wählt eine Liste von Knoten aus, die dem XPath-Ausdruck entsprechen. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Wählt den ersten[`Node`](../../aspose.words/node/) das dem XPath-Ausdruck entspricht. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Exportiert den Inhalt des Knotens in eine Zeichenfolge im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exportiert den Inhalt des Knotens unter Verwendung der angegebenen Speicheroptionen in eine Zeichenfolge. |

## Bemerkungen

Smarttags sind eine Art benutzerdefiniertes XML-Markup. Smarttags ermöglichen die Einbettung benutzerdefinierter Semantik in das Dokument, indem sie einen grundlegenden Namespace/Namen für einen Lauf oder eine Reihe von Läufen innerhalb eines Dokuments bereitstellen.

`SmartTag` kann ein Kind eines[`Paragraph`](../../aspose.words/paragraph/) oder ein anderes`SmartTag` Knoten.

Die vollständige Liste der untergeordneten Knoten, die innerhalb eines Smarttags vorkommen können, besteht aus [`BookmarkStart`](../../aspose.words/bookmarkstart/) ,[`BookmarkEnd`](../../aspose.words/bookmarkend/) , [`FieldStart`](../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator/) ,[`FieldEnd`](../../aspose.words.fields/fieldend/) ,[`FormField`](../../aspose.words.fields/formfield/) , [`Comment`](../../aspose.words/comment/) ,[`Footnote`](../../aspose.words.notes/footnote/) , [`Run`](../../aspose.words/run/) ,[`SpecialChar`](../../aspose.words/specialchar/) , [`Shape`](../../aspose.words.drawing/shape/) ,[`GroupShape`](../../aspose.words.drawing/groupshape/) , [`CommentRangeStart`](../../aspose.words/commentrangestart/) , [`CommentRangeEnd`](../../aspose.words/commentrangeend/) , `SmartTag`.

## Beispiele

Zeigt, wie Smarttags erstellt werden.

```csharp
public void Create()
{
    Document doc = new Document();

    // Ein Smarttag erscheint in einem Dokument, in dem Microsoft Word einen Teil des Textes als eine Art Daten erkennt.
    // wie etwa einen Namen, ein Datum oder eine Adresse, und wandelt es in einen Hyperlink um, der eine violette gepunktete Unterstreichung anzeigt.
    SmartTag smartTag = new SmartTag(doc);

    // Smarttags sind zusammengesetzte Knoten, die den erkannten Text vollständig enthalten.
    // Fügen Sie diesem Smarttag manuell Inhalte hinzu.
    smartTag.AppendChild(new Run(doc, "May 29, 2019"));

    // Microsoft Word erkennt den obigen Inhalt möglicherweise als Datum.
    // Smarttags verwenden die Eigenschaft „Element“, um den Typ der enthaltenen Daten widerzuspiegeln.
    smartTag.Element = "date";

    // Einige Smarttag-Typen verarbeiten ihren Inhalt weiter in benutzerdefinierte XML-Eigenschaften.
    smartTag.Properties.Add(new CustomXmlProperty("Day", string.Empty, "29"));
    smartTag.Properties.Add(new CustomXmlProperty("Month", string.Empty, "5"));
    smartTag.Properties.Add(new CustomXmlProperty("Year", string.Empty, "2019"));

    // Setzen Sie die URI des Smarttags auf den Standardwert.
    smartTag.Uri = "urn:schemas-microsoft-com:office:smarttags";

    doc.FirstSection.Body.FirstParagraph.AppendChild(smartTag);
    doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, " is a date. "));

    // Erstellen Sie ein weiteres Smarttag für einen Börsenticker.
    smartTag = new SmartTag(doc);
    smartTag.Element = "stockticker";
    smartTag.Uri = "urn:schemas-microsoft-com:office:smarttags";

    smartTag.AppendChild(new Run(doc, "MSFT"));

    doc.FirstSection.Body.FirstParagraph.AppendChild(smartTag);
    doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, " is a stock ticker."));

    // Drucken Sie alle Smarttags in unserem Dokument mithilfe eines Dokumentbesuchers.
    doc.Accept(new SmartTagPrinter());

    // Ältere Versionen von Microsoft Word unterstützen Smarttags.
    doc.Save(ArtifactsDir + "SmartTag.Create.doc");

    // Verwenden Sie die Methode „RemoveSmartTags“, um alle Smarttags aus einem Dokument zu entfernen.
    Assert.AreEqual(2, doc.GetChildNodes(NodeType.SmartTag, true).Count);

    doc.RemoveSmartTags();

    Assert.AreEqual(0, doc.GetChildNodes(NodeType.SmartTag, true).Count);
}

/// <summary>
/// Druckt besuchte Smarttags und deren Inhalte.
/// </summary>
private class SmartTagPrinter : DocumentVisitor
{
    /// <summary>
    /// Wird aufgerufen, wenn im Dokument ein SmartTag-Knoten gefunden wird.
    /// </summary>
    public override VisitorAction VisitSmartTagStart(SmartTag smartTag)
    {
        Console.WriteLine($"Smart tag type: {smartTag.Element}");
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn der Besuch eines SmartTag-Knotens beendet ist.
    /// </summary>
    public override VisitorAction VisitSmartTagEnd(SmartTag smartTag)
    {
        Console.WriteLine($"\tContents: \"{smartTag.ToString(SaveFormat.Text)}\"");

        if (smartTag.Properties.Count == 0)
        {
            Console.WriteLine("\tContains no properties");
        }
        else
        {
            Console.Write("\tProperties: ");
            string[] properties = new string[smartTag.Properties.Count];
            int index = 0;

            foreach (CustomXmlProperty cxp in smartTag.Properties)
                properties[index++] = $"\"{cxp.Name}\" = \"{cxp.Value}\"";

            Console.WriteLine(string.Join(", ", properties));
        }

        return VisitorAction.Continue;
    }
}
```

### Siehe auch

* class [CompositeNode](../../aspose.words/compositenode/)
* namensraum [Aspose.Words.Markup](../../aspose.words.markup/)
* Montage [Aspose.Words](../../)
