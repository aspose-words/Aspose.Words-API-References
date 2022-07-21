---
title: SmartTag
second_title: Aspose.Words für .NET-API-Referenz
description: Dieses Element gibt das Vorhandensein eines Smarttags um eine oder mehrere Inline-Strukturen Läufe Bilder Felder usw. innerhalb eines Absatzes an.
type: docs
weight: 3810
url: /de/net/aspose.words.markup/smarttag/
---
## SmartTag class

Dieses Element gibt das Vorhandensein eines Smarttags um eine oder mehrere Inline-Strukturen (Läufe, Bilder, Felder usw.) innerhalb eines Absatzes an.

```csharp
public class SmartTag : CompositeNode
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [SmartTag](smarttag)(DocumentBase) | Initialisiert eine neue Instanz von[`SmartTag`](../smarttag) Klasse. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | Ruft alle unmittelbar untergeordneten Knoten dieses Knotens ab. |
| [Count](../../aspose.words/compositenode/count) { get; } | Ruft die Anzahl der unmittelbaren Kinder dieses Knotens ab. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| virtual [Document](../../aspose.words/node/document) { get; } | Ruft das Dokument ab, zu dem dieser Knoten gehört. |
| [Element](../../aspose.words.markup/smarttag/element) { get; set; } | Gibt den Namen des Smarttags im Dokument an. |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | Ruft das erste untergeordnete Element des Knotens ab. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | Gibt wahr zurück, wenn dieser Knoten untergeordnete Knoten hat. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | Gibt wahr zurück, da dieser Knoten untergeordnete Knoten haben kann. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | Ruft das letzte untergeordnete Element des Knotens ab. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| override [NodeType](../../aspose.words.markup/smarttag/nodetype) { get; } | gibt zurück **NodeType.SmartTag** . |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Ruft den unmittelbar übergeordneten Knoten dieses Knotens ab. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Ruft den Knoten unmittelbar vor diesem Knoten ab. |
| [Properties](../../aspose.words.markup/smarttag/properties) { get; } | Eine Sammlung der Smarttag-Eigenschaften. |
| [Range](../../aspose.words/node/range) { get; } | Gibt a zurück **Bereich** Objekt, das den Teil eines Dokuments darstellt, das in diesem Knoten enthalten ist. |
| [Uri](../../aspose.words.markup/smarttag/uri) { get; set; } | Gibt den Namespace-URI des Smarttags an. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Accept](../../aspose.words.markup/smarttag/accept)(DocumentVisitor) | Akzeptiert einen Besucher. |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | Fügt den angegebenen Knoten am Ende der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [Clone](../../aspose.words/node/clone)(bool) | Erstellt ein Duplikat des Knotens. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | Reserviert für Systemnutzung. IXPfadNavigierbar. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Ruft den ersten Vorfahren der angegebenen ab[`NodeType`](../../aspose.words/nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Ruft den ersten Vorfahren des angegebenen Objekttyps ab. |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | Gibt einen N-ten untergeordneten Knoten zurück, der dem angegebenen Typ entspricht. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | Gibt eine Live-Sammlung von untergeordneten Knoten zurück, die dem angegebenen Typ entsprechen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | Bietet Unterstützung für die Iteration für jeden Stil über die untergeordneten Knoten dieses Knotens. |
| override [GetText](../../aspose.words/compositenode/gettext)() | Ruft den Text dieses Knotens und aller seiner Kinder ab. |
| [IndexOf](../../aspose.words/compositenode/indexof)(Node) | Gibt den Index des angegebenen untergeordneten Knotens im untergeordneten Knotenarray zurück. |
| [InsertAfter](../../aspose.words/compositenode/insertafter)(Node, Node) | Fügt den angegebenen Knoten unmittelbar nach dem angegebenen Referenzknoten ein. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore)(Node, Node) | Fügt den angegebenen Knoten unmittelbar vor dem angegebenen Referenzknoten ein. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Ruft den nächsten Knoten gemäß dem Traversalalgorithmus des Vorbestellungsbaums ab. |
| [PrependChild](../../aspose.words/compositenode/prependchild)(Node) | Fügt den angegebenen Knoten am Anfang der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Ruft den vorherigen Knoten gemäß dem Traversalalgorithmus des Vorbestellungsbaums ab. |
| [Remove](../../aspose.words/node/remove)() | Entfernt sich selbst vom übergeordneten Element. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren)() | Entfernt alle untergeordneten Knoten des aktuellen Knotens. |
| [RemoveChild](../../aspose.words/compositenode/removechild)(Node) | Entfernt den angegebenen untergeordneten Knoten. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags)() | Entfernt alle[`SmartTag`](../smarttag) Nachkommenknoten des aktuellen Knotens. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes)(string) | Wählt eine Liste von Knoten aus, die mit dem XPath-Ausdruck übereinstimmen. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode)(string) | Wählt den ersten Knoten aus, der mit dem XPath-Ausdruck übereinstimmt. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Exportiert den Inhalt des Knotens in einen String im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Exportiert den Inhalt des Knotens unter Verwendung der angegebenen Speicheroptionen in einen String. |

### Bemerkungen

Smarttags sind eine Art benutzerdefiniertes XML-Markup. Smart-Tags bieten eine Möglichkeit zum Einbetten einer kundendefinierten Semantik in das Dokument über die Fähigkeit, einen grundlegenden Namensraum/Namen für einen Lauf oder eine Reihe von Läufen innerhalb eines Dokuments bereitzustellen.

[`SmartTag`](../smarttag) kann ein Kind von a sein[`Paragraph`](../../aspose.words/paragraph) or ein anderer[`SmartTag`](../smarttag) Knoten.

Die vollständige Liste der untergeordneten Knoten, die in einem Smarttag vorkommen können, besteht aus [`BookmarkStart`](../../aspose.words/bookmarkstart) ,[`BookmarkEnd`](../../aspose.words/bookmarkend) , [`FieldStart`](../../aspose.words.fields/fieldstart) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator) ,[`FieldEnd`](../../aspose.words.fields/fieldend) ,[`FormField`](../../aspose.words.fields/formfield) , [`Comment`](../../aspose.words/comment) ,[`Footnote`](../../aspose.words.notes/footnote) , [`Run`](../../aspose.words/run) ,[`SpecialChar`](../../aspose.words/specialchar) , [`Shape`](../../aspose.words.drawing/shape) ,[`GroupShape`](../../aspose.words.drawing/groupshape) , [`CommentRangeStart`](../../aspose.words/commentrangestart) , [`CommentRangeEnd`](../../aspose.words/commentrangeend) , [`SmartTag`](../smarttag).

### Beispiele

Zeigt, wie Smarttags erstellt werden.

```csharp
public void Create()
{
    Document doc = new Document();

    // Ein Smart Tag erscheint in einem Dokument mit Microsoft Word erkennt einen Teil seines Textes als irgendeine Form von Daten,
    // wie Name, Datum oder Adresse, und wandelt sie in einen Hyperlink um, der eine violett gepunktete Unterstreichung anzeigt.
    SmartTag smartTag = new SmartTag(doc);

    // Smarttags sind zusammengesetzte Knoten, die ihren erkannten Text vollständig enthalten.
    // Inhalte manuell zu diesem Smart Tag hinzufügen.
    smartTag.AppendChild(new Run(doc, "May 29, 2019"));

    // Microsoft Word kann den obigen Inhalt als Datum erkennen.
    // Smarttags verwenden die "Element"-Eigenschaft, um die Art der Daten widerzuspiegeln, die sie enthalten.
    smartTag.Element = "date";

    // Einige Smarttag-Typen verarbeiten ihren Inhalt weiter in benutzerdefinierte XML-Eigenschaften.
    smartTag.Properties.Add(new CustomXmlProperty("Day", string.Empty, "29"));
    smartTag.Properties.Add(new CustomXmlProperty("Month", string.Empty, "5"));
    smartTag.Properties.Add(new CustomXmlProperty("Year", string.Empty, "2019"));

    // Den URI des Smarttags auf den Standardwert setzen.
    smartTag.Uri = "urn:schemas-microsoft-com:office:smarttags";

    doc.FirstSection.Body.FirstParagraph.AppendChild(smartTag);
    doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, " is a date. "));

    // Erstellen Sie ein weiteres Smart Tag für einen Börsenticker.
    smartTag = new SmartTag(doc);
    smartTag.Element = "stockticker";
    smartTag.Uri = "urn:schemas-microsoft-com:office:smarttags";

    smartTag.AppendChild(new Run(doc, "MSFT"));

    doc.FirstSection.Body.FirstParagraph.AppendChild(smartTag);
    doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, " is a stock ticker."));

    // Alle Smart-Tags in unserem Dokument mit einem Dokumentbesucher drucken.
    doc.Accept(new SmartTagPrinter());

    // Ältere Versionen von Microsoft Word unterstützen Smart Tags.
    doc.Save(ArtifactsDir + "SmartTag.Create.doc");

    // Verwenden Sie die Methode "RemoveSmartTags", um alle Smarttags aus einem Dokument zu entfernen.
    Assert.AreEqual(2, doc.GetChildNodes(NodeType.SmartTag, true).Count);

    doc.RemoveSmartTags();

    Assert.AreEqual(0, doc.GetChildNodes(NodeType.SmartTag, true).Count);
}

/// <summary>
/// Druckt besuchte Smarttags und deren Inhalt.
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

* class [CompositeNode](../../aspose.words/compositenode)
* namensraum [Aspose.Words.Markup](../../aspose.words.markup)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
