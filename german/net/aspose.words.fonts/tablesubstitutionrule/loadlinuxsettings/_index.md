---
title: TableSubstitutionRule.LoadLinuxSettings
linktitle: LoadLinuxSettings
articleTitle: LoadLinuxSettings
second_title: Aspose.Words für .NET
description: Laden Sie mühelos vordefinierte Tabellensubstitutionseinstellungen für Linux mit der Methode LoadLinuxSettings. Optimieren Sie Ihren Workflow noch heute!
type: docs
weight: 50
url: /de/net/aspose.words.fonts/tablesubstitutionrule/loadlinuxsettings/
---
## TableSubstitutionRule.LoadLinuxSettings method

Lädt vordefinierte Tabellensubstitutionseinstellungen für die Linux-Plattform.

```csharp
public void LoadLinuxSettings()
```

## Beispiele

Zeigt, wie auf Schriftartenersetzungstabellen für Windows und Linux zugegriffen wird.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Erstellen Sie eine neue Tabellenersetzungsregel und laden Sie die standardmäßige Schriftartersetzungstabelle von Microsoft Windows.
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;
tableSubstitutionRule.LoadWindowsSettings();

// Unter Windows ist „Times New Roman“ der Standardersatz für die Schriftart „Times New Roman CE“.
Assert.AreEqual(new[] {"Times New Roman"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// Wir können die Tabelle in Form eines XML-Dokuments speichern.
tableSubstitutionRule.Save(ArtifactsDir + "FontSettings.TableSubstitutionRule.Windows.xml");

// Linux hat eine eigene Substitutionstabelle.
// Es gibt mehrere Ersatzschriften für „Times New Roman CE“.
// Wenn der erste Ersatz, „FreeSerif“, auch nicht verfügbar ist,
// Diese Regel durchläuft die anderen im Array, bis sie eine verfügbare findet.
tableSubstitutionRule.LoadLinuxSettings();
Assert.AreEqual(new[] {"FreeSerif", "Liberation Serif", "DejaVu Serif"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// Speichern Sie die Linux-Substitutionstabelle mithilfe eines Streams in Form eines XML-Dokuments.
using (FileStream fileStream = new FileStream(ArtifactsDir + "FontSettings.TableSubstitutionRule.Linux.xml",
    FileMode.Create))
{
    tableSubstitutionRule.Save(fileStream);
}
```

### Siehe auch

* class [TableSubstitutionRule](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)
