---
title: "Aspose::Words::Range::UpdateFields Methode"
linktitle: "UpdateFields"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Range::UpdateFields Methode. Aktualisiert die Werte von Dokumentfeldern in diesem Bereich, in C++."
type: docs
weight: 15000
url: /de/cpp/aspose.words/range/updatefields/
---
## Range::UpdateFields method


Aktualisiert die Werte von Dokumentfeldern in diesem Bereich.

```cpp
void Aspose::Words::Range::UpdateFields()
```

## Hinweise


Wenn Sie ein Dokument öffnen, ändern und anschließend speichern, aktualisiert Aspose.Words die Felder nicht automatisch, sondern lässt sie unverändert. Daher sollten Sie diese Methode in der Regel vor dem Speichern aufrufen, wenn Sie das Dokument programmgesteuert geändert haben und sicherstellen möchten, dass die korrekten (berechneten) Feldwerte im gespeicherten Dokument erscheinen.

Es ist nicht erforderlich, Felder nach dem Ausführen eines Seriendrucks zu aktualisieren, da der Seriendruck eine Art Feldaktualisierung ist und automatisch alle Felder im Dokument aktualisiert.

Diese Methode aktualisiert nicht alle Feldtypen. Für die detaillierte Liste der unterstützten Feldtypen siehe das Programmierhandbuch.

Diese Methode aktualisiert keine Felder, die mit den Seitenlayout‑Algorithmen (z. B. PAGE, PAGES, PAGEREF) zusammenhängen. Die seitenlayoutbezogenen Felder werden aktualisiert, wenn Sie ein Dokument rendern oder [UpdatePageLayout](../../document/updatepagelayout/) aufrufen.

Um Felder im gesamten Dokument zu aktualisieren, verwenden Sie [UpdateFields](../../document/updatefields/).

## Beispiele



Zeigt, wie man alle Felder in einem Bereich aktualisiert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertField(u" DOCPROPERTY Category");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakEvenPage);
builder->InsertField(u" DOCPROPERTY Category");

// Die obigen DOCPROPERTY‑Felder zeigen den Wert dieser integrierten Dokumenteigenschaft an.
doc->get_BuiltInDocumentProperties()->set_Category(u"MyCategory");

// Wenn wir den Wert einer Dokumenteigenschaft aktualisieren, müssen wir alle DOCPROPERTY‑Felder aktualisieren, damit sie ihn anzeigen.
ASSERT_EQ(System::String::Empty, doc->get_Range()->get_Fields()->idx_get(0)->get_Result());
ASSERT_EQ(System::String::Empty, doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

// Aktualisieren Sie alle Felder, die im Bereich des ersten Abschnitts liegen.
doc->get_FirstSection()->get_Range()->UpdateFields();

ASSERT_EQ(u"MyCategory", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());
ASSERT_EQ(System::String::Empty, doc->get_Range()->get_Fields()->idx_get(1)->get_Result());
```

## Siehe auch

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
