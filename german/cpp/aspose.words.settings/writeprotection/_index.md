---
title: "Aspose::Words::Settings::WriteProtection Klasse"
linktitle: "WriteProtection"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Settings::WriteProtection Klasse. Gibt die Einstellungen für den Schreibschutz eines Dokuments an. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 10000
url: /de/cpp/aspose.words.settings/writeprotection/
---
## WriteProtection class


Gibt die Schreibschutz‑Einstellungen für ein Dokument an. Weitere Informationen finden Sie im Dokumentationsartikel [Dokument schützen oder verschlüsseln](https://docs.aspose.com/words/cpp/protect-or-encrypt-a-document/).

```cpp
class WriteProtection : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_IsWriteProtected](./get_iswriteprotected/)() | Gibt **true** zurück, wenn ein Schreibschutz-Passwort festgelegt ist. |
| [get_ReadOnlyRecommended](./get_readonlyrecommended/)() const | Gibt an, ob der Dokumentautor empfohlen hat, das Dokument schreibgeschützt zu öffnen. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ReadOnlyRecommended](./set_readonlyrecommended/)(bool) | Setter für [Aspose::Words::Settings::WriteProtection::get_ReadOnlyRecommended](./get_readonlyrecommended/). |
| [SetPassword](./setpassword/)(const System::String\&) | Legt das Schreibschutz-Passwort für das Dokument fest. |
| static [Type](./type/)() |  |
| [ValidatePassword](./validatepassword/)(const System::String\&) | Gibt **true** zurück, wenn das angegebene Passwort dem Schreibschutz-Passwort entspricht, mit dem das Dokument geschützt wurde. Ist das Dokument nicht passwortgeschützt, wird **false** zurückgegeben. |
## Hinweise


Der Schreibschutz gibt an, ob der Autor empfohlen hat, das Dokument schreibgeschützt zu öffnen und/oder ein Passwort zum Ändern des Dokuments erforderlich ist.

Schreibschutz unterscheidet sich vom Dokumentenschutz. Schreibschutz wird in Microsoft Word in den Optionen des Dialogfelds "Speichern unter" festgelegt.

Sie erstellen keine Instanzen dieser Klasse direkt. Sie greifen über die Eigenschaft [WriteProtection](../../aspose.words/document/get_writeprotection/) auf die Dokumentenschutz-Einstellungen zu.

## Beispiele



Zeigt, wie ein Dokument mit einem Passwort geschützt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world! This document is protected.");

// Geben Sie ein Passwort mit einer Länge von bis zu 15 Zeichen ein und überprüfen Sie anschließend den Schutzstatus des Dokuments.
doc->get_WriteProtection()->SetPassword(u"MyPassword");
doc->get_WriteProtection()->set_ReadOnlyRecommended(true);

ASSERT_TRUE(doc->get_WriteProtection()->get_IsWriteProtected());
ASSERT_TRUE(doc->get_WriteProtection()->ValidatePassword(u"MyPassword"));

// Der Schutz verhindert nicht, dass das Dokument programmgesteuert bearbeitet wird, und verschlüsselt den Inhalt nicht.
doc->Save(get_ArtifactsDir() + u"Document.WriteProtection.docx");
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.WriteProtection.docx");

ASSERT_TRUE(doc->get_WriteProtection()->get_IsWriteProtected());

builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->Writeln(u"Writing text in a protected document.");

ASSERT_EQ(System::String(u"Hello world! This document is protected.") + u"\rWriting text in a protected document.", doc->GetText().Trim());
```

## Siehe auch

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
