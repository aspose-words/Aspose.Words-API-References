---
title: "Aspose::Words::Settings::ViewType Enum"
linktitle: "ViewType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Settings::ViewType Enum. Mögliche Werte für den Ansichtsmodus in Microsoft Word in C++."
type: docs
weight: 21000
url: /de/cpp/aspose.words.settings/viewtype/
---
## ViewType enum


Mögliche Werte für den Ansichtsmodus in Microsoft Word.

```cpp
enum class ViewType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Keine | 0 | Das Dokument soll in der Standardansicht der Anwendung gerendert werden. |
| Reading | 0 | Das Dokument soll in der Standardansicht der Anwendung gerendert werden. |
| PageLayout | 1 | Das Dokument soll in einer Ansicht geöffnet werden, die das Dokument so anzeigt, wie es gedruckt wird. |
| Umriss | 3 | Das Dokument soll in einer Ansicht gerendert werden, die für Gliederungen oder das Erstellen langer Dokumente optimiert ist. |
| Normal | 4 | Das Dokument soll in einer Ansicht gerendert werden, die für Gliederungen oder das Erstellen langer Dokumente optimiert ist. |
| Web | 5 | Das Dokument soll in einer Ansicht gerendert werden, die die Art und Weise nachahmt, wie dieses Dokument in einer Webseite angezeigt würde. |


## Beispiele



Zeigt, wie ein benutzerdefinierter Zoomfaktor festgelegt wird, den ältere Versionen von Microsoft Word beim Laden eines Dokuments anwenden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

doc->get_ViewOptions()->set_ViewType(Aspose::Words::Settings::ViewType::PageLayout);
doc->get_ViewOptions()->set_ZoomPercent(50);

ASSERT_EQ(Aspose::Words::Settings::ZoomType::Custom, doc->get_ViewOptions()->get_ZoomType());
ASSERT_EQ(Aspose::Words::Settings::ZoomType::None, doc->get_ViewOptions()->get_ZoomType());

doc->Save(get_ArtifactsDir() + u"ViewOptions.SetZoomPercentage.doc");
```

## Siehe auch

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
