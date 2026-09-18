---
title: "Aspose::Words::Layout::PageLayoutEvent enum"
linktitle: "PageLayoutEvent"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Layout::PageLayoutEvent enum. Ein Ereigniscodes, der während des Aufbaus und Renderns des Seitenlayout‑Modells ausgelöst wird. Das Seitenlayout‑Modell wird in zwei Schritten erstellt. Erstens der \\\"conversion step\\\", bei dem das Seitenlayout den Dokumentinhalt abruft und einen Objektgraphen erzeugt. Zweitens der \\\"reflow step\\\", bei dem Strukturen aufgeteilt, zusammengeführt und zu Seiten angeordnet werden. Je nach der Operation, die den Aufbau ausgelöst hat, kann das Seitenlayout‑Modell weiter in ein festes Seitenformat gerendert werden oder nicht. Beispielsweise erfordern das Berechnen der Seitenzahl im Dokument oder das Aktualisieren von Feldern kein Rendering, während der Export nach PDF dies in C++ tut."
type: docs
weight: 10000
url: /de/cpp/aspose.words.layout/pagelayoutevent/
---
## PageLayoutEvent enum


Ein Ereigniscodes, der während des Aufbaus und der Renderung des Seitenlayoutmodells ausgelöst wird. Das Seitenlayoutmodell wird in zwei Schritten erstellt. Erstens der "conversion step", dabei zieht das Seitenlayout den Dokumentinhalt und erstellt einen Objektgraphen. Zweitens der "reflow step", dabei werden Strukturen aufgeteilt, zusammengeführt und zu Seiten angeordnet. Abhängig von der Operation, die den Aufbau ausgelöst hat, kann das Seitenlayoutmodell weiter in ein festes Seitenformat gerendert werden oder nicht. Zum Beispiel erfordert das Berechnen der Seitenzahl im Dokument oder das Aktualisieren von Feldern keine Renderung, während der Export nach PDF dies tut.

```cpp
enum class PageLayoutEvent
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Keine | 0 | Standardwert. |
| WatchDog | 1 | Entspricht einem Prüfpunkt im Code, der häufig besucht wird und sich zum Abbrechen des Vorgangs eignet. Während Sie sich innerhalb von [Notify()](../ipagelayoutcallback/notify/) befinden, werfen Sie eine benutzerdefinierte Ausnahme, um den Vorgang abzubrechen. Sie können beim Umgang mit jedem Callback‑Ereignis eine Ausnahme werfen, um den Vorgang abzubrechen. Beachten Sie, dass bei einem Abbruch der Vorgang das Seitenlayout‑Modell in einen undefinierten Zustand versetzt. Wenn der Vorgang jedoch beim Reflow einer vollständigen Seite abgebrochen wird, sollte es möglich sein, das Layout‑Modell bis zum Ende dieser Seite zu verwenden. |
| BuildStarted | 2 | Der Aufbau des Seitenlayouts hat begonnen. Einmal ausgelöst. Dies ist das erste Ereignis, das auftritt, wenn [UpdatePageLayout](../../aspose.words/document/updatepagelayout/) aufgerufen wird. |
| BuildFinished | 3 | Der Aufbau des Seitenlayouts ist abgeschlossen. Einmal ausgelöst. Dies ist das letzte Ereignis, das auftritt, wenn [UpdatePageLayout](../../aspose.words/document/updatepagelayout/) aufgerufen wird. |
| ConversionStarted | 4 | Die Konvertierung des Dokumentmodells zum Seitenlayout hat begonnen. Einmal ausgelöst. Dies geschieht, wenn das Layout‑Modell beginnt, den Dokumentinhalt abzurufen. |
| ConversionFinished | 5 | Die Konvertierung des Dokumentmodells zum Seitenlayout ist abgeschlossen. Einmal ausgelöst. Dies geschieht, wenn das Layout‑Modell aufhört, den Dokumentinhalt abzurufen. |
| ReflowStarted | 6 | Der Reflow des Seitenlayouts hat begonnen. Einmal ausgelöst. Dies geschieht, wenn das Layout‑Modell beginnt, den Dokumentinhalt zu reflowen. |
| ReflowFinished | 7 | Der Reflow des Seitenlayouts ist abgeschlossen. Einmal ausgelöst. Dies geschieht, wenn das Layout‑Modell aufhört, den Dokumentinhalt zu reflowen. |
| PartReflowStarted | 8 | Das Neufließen der Seite hat begonnen. Beachten Sie, dass die Seite mehrfach neu fließen kann und dass das Neufließen neu starten kann, bevor es abgeschlossen ist. |
| PartReflowFinished | 9 | Das Neufließen der Seite ist abgeschlossen. Beachten Sie, dass die Seite mehrfach neu fließen kann und dass das Neufließen neu starten kann, bevor es abgeschlossen ist. |
| PartRenderingStarted | 10 | [Rendering](../../aspose.words.rendering/) der Seite hat begonnen. Dies wird einmal pro Seite ausgelöst. |
| PartRenderingFinished | 11 | [Rendering](../../aspose.words.rendering/) der Seite ist abgeschlossen. Dies wird einmal pro Seite ausgelöst. |

## Siehe auch

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
