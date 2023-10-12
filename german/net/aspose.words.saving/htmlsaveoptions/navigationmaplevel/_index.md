---
title: HtmlSaveOptions.NavigationMapLevel
second_title: Aspose.Words für .NET-API-Referenz
description: HtmlSaveOptions eigendom. Gibt die maximale Anzahl von Überschriften an die beim Export in die Formate EPUB MOBI oder AZW3 in die Navigationskarte eingefügt werden. Der Standardwert ist3 .
type: docs
weight: 390
url: /de/net/aspose.words.saving/htmlsaveoptions/navigationmaplevel/
---
## HtmlSaveOptions.NavigationMapLevel property

Gibt die maximale Anzahl von Überschriften an, die beim Export in die Formate EPUB, MOBI oder AZW3 in die Navigationskarte eingefügt werden. Der Standardwert ist`3` .

```csharp
public int NavigationMapLevel { get; set; }
```

### Bemerkungen

Die Navigationskarte ermöglicht Benutzeragenten eine einfache Navigation durch die Dokumentstruktur. Normalerweise entsprechen Navigationspunkte Überschriften im Dokument. Um Überschriften bis zur Ebene zu füllen **N** diesen Wert zuweisen`NavigationMapLevel`.

Standardmäßig werden drei Überschriftenebenen ausgefüllt: Absätze von Stilen **Überschrift 1** , **Überschrift 2** und **Überschrift 3**. Sie können diese Eigenschaft auf einen Wert von 1 bis 9 setzen, um die entsprechende maximale Ebene anzufordern. Wenn Sie sie auf Null setzen, wird die Navigationskarte nur auf den Dokumentstamm oder die Wurzeln von Dokumentteilen reduziert.

### Siehe auch

* class [HtmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../htmlsaveoptions/)
* Montage [Aspose.Words](../../../)


