---
title: "Aspose::Words::ImportFormatMode Enum"
linktitle: "ImportFormatMode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ImportFormatMode Enum. Gibt an, wie Formatierungen beim Importieren von Inhalten aus einem anderen Dokument in C++ zusammengeführt werden."
type: docs
weight: 93000
url: /de/cpp/aspose.words/importformatmode/
---
## ImportFormatMode enum


Gibt an, wie die Formatierung beim Importieren von Inhalten aus einem anderen Dokument zusammengeführt wird.

```cpp
enum class ImportFormatMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| UseDestinationStyles | 0 | Verwenden Sie die Stile des Ziel Dokuments und kopieren Sie neue Stile. Dies ist die Standardoption. |
| KeepSourceFormatting | 1 | Kopieren Sie alle erforderlichen Formatvorlagen in das Ziel-Dokument, erzeugen Sie bei Bedarf eindeutige Formatvorlagennamen. |
| KeepDifferentStyles | 2 | Nur Formatvorlagen kopieren, die sich von denen im Quell-Dokument unterscheiden. |

## Hinweise


Wenn Sie Knoten von einem Dokument in ein anderes kopieren, legt diese Option fest, wie die Formatierung aufgelöst wird, wenn beide Dokumente eine Formatvorlage mit demselben Namen, aber unterschiedlicher Formatierung besitzen.

Die Formatierung wird wie folgt aufgelöst:

1. Eingebaute Formatvorlagen werden anhand ihrer lokalisierungsunabhängigen Stil-ID zugeordnet. Benutzerdefinierte Formatvorlagen werden anhand eines case‑sensitiven Stilnamens zugeordnet.
1. Wird im Ziel-Dokument keine passende Formatvorlage gefunden, wird die Formatvorlage (und alle von ihr referenzierten Formatvorlagen) in das Ziel-Dokument kopiert und die importierten Knoten werden aktualisiert, um auf die neue Formatvorlage zu verweisen.
1. Wenn im Ziel-Dokument bereits eine passende Formatvorlage existiert, hängt das weitere Vorgehen vom Parameter **importFormatMode** ab, der an [ImportNode()](../) übergeben wird, wie unten beschrieben.



Beim Verwenden der Option [UseDestinationStyles](./) wird, wenn im Ziel-Dokument bereits eine passende Formatvorlage existiert, die Formatvorlage nicht kopiert und die importierten Knoten werden aktualisiert, um auf die vorhandene Formatvorlage zu verweisen.

Der Nachteil der Verwendung von [UseDestinationStyles](./) besteht darin, dass der importierte Text im Ziel-Dokument im Vergleich zum Quell-Dokument anders aussehen kann. Zum Beispiel verwendet die Formatvorlage "Heading 1" im Quell-Dokument die Schriftart Arial 16pt, während die Formatvorlage "Heading 1" im Ziel-Dokument die Schriftart Times New Roman 14pt verwendet. Beim Importieren von Text mit der Formatvorlage "Heading 1" ohne weitere direkte Formatierung erscheint er im Ziel-Dokument als Times New Roman 14pt.

[KeepSourceFormatting](./) option allows to make sure the imported content looks the same in the destination document like it looks in the source document. If a matching style already exists in the destination document, the source style formatting is expanded into direct [Node](../node/) attributes and the style is changed to Normal. If the style does not exist in the destination document, then the source style is imported into the destination document and applied to the imported node. Note, that it is not always possible to preserve the source style even if it does not exist in the destination document. In this case formatting of such style will be expanded into direct [Node](../node/) attributes in favor of preserving original [Node](../node/) formatting.

Der Nachteil der Verwendung von [KeepSourceFormatting](./) besteht darin, dass bei mehreren Importen viele Formatvorlagen im Ziel-Dokument entstehen können, was die einheitliche Formatierung in Microsoft Word für dieses Dokument erschwert.

Die Verwendung der Option [KeepDifferentStyles](./) ermöglicht die Wiederverwendung von Ziel-Formatvorlagen, wenn deren Formatierung mit der der Formatvorlagen im Quell-Dokument identisch ist. Ist die Formatvorlage im Ziel-Dokument jedoch anders als im Quell-Dokument, wird sie importiert.

## Beispiele



Zeigt, wie ein Dokument in ein anderes Dokument eingefügt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

auto docToInsert = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Formatted elements.docx");

builder->InsertDocument(docToInsert, Aspose::Words::ImportFormatMode::KeepSourceFormatting);
builder->get_Document()->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertDocument.docx");
```

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
