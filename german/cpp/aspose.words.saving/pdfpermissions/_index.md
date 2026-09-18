---
title: "Aspose::Words::Saving::PdfPermissions Aufzählung"
linktitle: "PdfPermissions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::PdfPermissions Aufzählung. Gibt die Vorgänge an, die einem Benutzer an einem verschlüsselten PDF-Dokument in C++ erlaubt sind."
type: docs
weight: 80000
url: /de/cpp/aspose.words.saving/pdfpermissions/
---
## PdfPermissions enum


Gibt die Vorgänge an, die einem Benutzer an einem verschlüsselten PDF-Dokument erlaubt sind.

```cpp
enum class PdfPermissions
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| DisallowAll | 0 | Verweigert alle Vorgänge am PDF-Dokument. Dies ist der Standardwert. |
| AllowAll | 65535 | Erlaubt alle Vorgänge am PDF-Dokument. |
| ContentCopy | n/a | Kopieren oder anderweitiges Extrahieren von Text und Grafiken aus dem Dokument durch Vorgänge, die nicht von [ContentCopyForAccessibility](./) gesteuert werden. |
| ContentCopyForAccessibility | n/a | Extrahieren von Text und Grafiken (zur Unterstützung der Barrierefreiheit für Nutzer mit Behinderungen oder zu anderen Zwecken). |
| ModifyContents | n/a | Den Inhalt des Dokuments durch Vorgänge ändern, die nicht von [ModifyAnnotations](./), [FillIn](./) und [DocumentAssembly](./) gesteuert werden. |
| ModifyAnnotations | n/a | Textanmerkungen hinzufügen oder ändern, interaktive Formularfelder ausfüllen und, falls [ModifyContents](./) ebenfalls gesetzt ist, interaktive Formularfelder (einschließlich Signaturfelder) erstellen oder ändern. |
| FillIn | n/a | Vorhandene interaktive Formularfelder (einschließlich Signaturfelder) ausfüllen, selbst wenn [ModifyContents](./) nicht gesetzt ist. |
| DocumentAssembly | n/a | Das Dokument zusammenstellen (Seiten einfügen, drehen oder löschen und Gliederungspunkte oder Miniaturbilder erstellen), selbst wenn [ModifyContents](./) nicht gesetzt ist. |
| Printing | n/a | Das Dokument drucken (möglicherweise nicht in höchster Qualität, abhängig davon, ob [HighResolutionPrinting](./) ebenfalls gesetzt ist). |
| HighResolutionPrinting | n/a | Das Dokument in eine Darstellung drucken, aus der eine getreue digitale Kopie des PDF-Inhalts erzeugt werden kann, basierend auf einem implementierungsabhängigen Algorithmus. Wenn dieses Flag nicht gesetzt ist (und [Printing](./) gesetzt ist), ist der Druck auf eine niedrigstufige Darstellung des Erscheinungsbildes zu beschränken, möglicherweise in verminderter Qualität. |

## Siehe auch

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
