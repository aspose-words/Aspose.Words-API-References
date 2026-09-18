---
title: "Aspose::Words::NodeImporter‑Klasse"
linktitle: "NodeImporter"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::NodeImporter‑Klasse. Ermöglicht das effiziente wiederholte Importieren von Knoten von einem Dokument in ein anderes. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 44000
url: /de/cpp/aspose.words/nodeimporter/
---
## NodeImporter class


Ermöglicht das effiziente wiederholte Importieren von Knoten von einem Dokument in ein anderes. Weitere Informationen finden Sie im Dokumentationsartikel [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class NodeImporter : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [ImportNode](./importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | Importiert einen Knoten von einem Dokument in ein anderes. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NodeImporter](./nodeimporter/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::ImportFormatMode) | Initialisiert eine neue Instanz der Klasse [NodeImporter](./). |
| [NodeImporter](./nodeimporter/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | Initialisiert eine neue Instanz der Klasse [NodeImporter](./). |
| static [Type](./type/)() |  |
## Hinweise


Aspose.Words bietet Funktionen zum einfachen Kopieren und Verschieben von Fragmenten zwischen Microsoft‑Word‑Dokumenten. Dies wird als "Knoten importieren" bezeichnet. Bevor Sie ein Fragment von einem Dokument in ein anderes einfügen können, müssen Sie es "importieren". Der Import erzeugt einen tiefen Klon des ursprünglichen Knotens, der in das Zieldokument eingefügt werden kann.

Der einfachste Weg, einen Knoten zu importieren, besteht darin, die Methode [ImportNode()](../) zu verwenden, die vom Objekt [DocumentBase](../documentbase/) bereitgestellt wird.

Wenn Sie jedoch Knoten mehrfach von einem Dokument in ein anderes importieren müssen, ist es besser, die Klasse [NodeImporter](./) zu verwenden. Die Klasse [NodeImporter](./) ermöglicht es, die Anzahl der im Zieldokument erstellten Formatvorlagen und Listen zu minimieren.

Das Kopieren oder Verschieben von Fragmenten von einem Microsoft‑Word‑Dokument in ein anderes stellt Aspose.Words vor mehrere technische Herausforderungen. In einem Word‑Dokument werden Formatvorlagen und Listformatierungen zentral und getrennt vom Text des Dokuments gespeichert. Die Absätze und Textläufe verweisen lediglich über interne eindeutige Kennungen auf die Formatvorlagen.

Die Herausforderungen ergeben sich daraus, dass Formatvorlagen und Listen in verschiedenen Dokumenten unterschiedlich sind. Beispielsweise müssen beim Kopieren eines Absatzes, der mit der Formatvorlage Überschrift 1 formatiert ist, mehrere Aspekte berücksichtigt werden: Entscheiden, ob die Formatvorlage Überschrift 1 vom Quell‑ in das Zieldokument kopiert werden soll, den Absatz klonen, den geklonten Absatz so aktualisieren, dass er auf die korrekte Formatvorlage Überschrift 1 im Zieldokument verweist. Wenn die Formatvorlage kopiert werden muss, sollten alle von ihr referenzierten Formatvorlagen (basierend auf Formatvorlage und nächstem Absatzstil) analysiert und ggf. ebenfalls kopiert werden usw. Ähnliche Probleme treten beim Kopieren von Aufzählungs‑ oder Nummerierungs‑Absätzen auf, da Microsoft Word Listendefinitionen getrennt vom Text speichert.

Die Klasse [NodeImporter](./) fungiert wie ein Kontext, der während des Imports die "Übersetzungstabellen" enthält. Sie übersetzt korrekt zwischen Formatvorlagen und Listen im Quell‑ und Zieldokument.

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
