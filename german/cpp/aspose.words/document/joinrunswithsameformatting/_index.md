---
title: "Aspose::Words::Document::JoinRunsWithSameFormatting Methode"
linktitle: "JoinRunsWithSameFormatting"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::JoinRunsWithSameFormatting Methode. Fügt Runs mit gleicher Formatierung in allen Absätzen des Dokuments in C++ zusammen."
type: docs
weight: 65000
url: /de/cpp/aspose.words/document/joinrunswithsameformatting/
---
## Document::JoinRunsWithSameFormatting method


Führt Läufe mit gleicher Formatierung in allen Absätzen des Dokuments zusammen.

```cpp
int32_t Aspose::Words::Document::JoinRunsWithSameFormatting()
```


### ReturnValue

Anzahl der durchgeführten Zusammenführungen. Wenn **N** benachbarte Runs zusammengeführt werden, zählen sie als **N - 1** Zusammenführungen.
## Hinweise


Dies ist eine Optimierungsmethode. Einige Dokumente enthalten benachbarte Runs mit gleicher Formatierung. Normalerweise tritt dies auf, wenn ein Dokument intensiv manuell bearbeitet wurde. Sie können die Dokumentgröße reduzieren und die weitere Verarbeitung beschleunigen, indem Sie diese Runs zusammenführen.

Der Vorgang prüft jeden [Paragraph](../../paragraph/) Knoten im Dokument auf benachbarte [Run](../../run/) Knoten mit identischen Eigenschaften. Er ignoriert eindeutige Kennungen, die zur Verfolgung von Bearbeitungssitzungen bei der Erstellung und Änderung von Runs verwendet werden. Der erste Run in jeder Zusammenführungssequenz sammelt den gesamten Text. Die übrigen Runs werden aus dem Dokument gelöscht.

## Beispiele



Zeigt, wie Runs in einem Dokument zusammengeführt werden, um unnötige Runs zu reduzieren.
```cpp
// Öffnen Sie ein Dokument, das benachbarte Text‑Runs mit identischer Formatierung enthält,
// was häufig vorkommt, wenn wir denselben Absatz mehrfach in Microsoft Word bearbeiten.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Wenn beliebig viele dieser Runs benachbart mit identischer Formatierung sind,
// kann das Dokument vereinfacht werden.
ASSERT_EQ(317, doc->GetChildNodes(Aspose::Words::NodeType::Run, true)->get_Count());

// Kombinieren Sie solche Runs mit dieser Methode und überprüfen Sie die Anzahl der Run‑Zusammenführungen, die stattfinden werden.
ASSERT_EQ(121, doc->JoinRunsWithSameFormatting());

// Die Anzahl der Zusammenführungen und die Anzahl der Runs, die wir nach der Zusammenführung haben
// sollte der Anzahl der Runs entsprechen, die wir ursprünglich hatten.
ASSERT_EQ(196, doc->GetChildNodes(Aspose::Words::NodeType::Run, true)->get_Count());
```

## Siehe auch

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
