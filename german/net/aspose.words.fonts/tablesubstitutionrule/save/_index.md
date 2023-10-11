---
title: TableSubstitutionRule.Save
second_title: Aspose.Words für .NET-API-Referenz
description: TableSubstitutionRule methode. Speichert die aktuellen Tabellenersetzungseinstellungen in der Datei.
type: docs
weight: 70
url: /de/net/aspose.words.fonts/tablesubstitutionrule/save/
---
## Save(string) {#save_1}

Speichert die aktuellen Tabellenersetzungseinstellungen in der Datei.

```csharp
public void Save(string fileName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | String | Name der Ausgabedatei. |

### Beispiele

Zeigt, wie man auf Schriftarten-Ersetzungstabellen für Windows und Linux zugreift.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Erstellen Sie eine neue Tabellenersetzungsregel und laden Sie die Standard-Schriftartenersetzungstabelle von Microsoft Windows.
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;
tableSubstitutionRule.LoadWindowsSettings();

// In Windows ist der Standardersatz für die Schriftart „Times New Roman CE“ „Times New Roman“.
Assert.AreEqual(new[] {"Times New Roman"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// Wir können die Tabelle in Form eines XML-Dokuments speichern.
tableSubstitutionRule.Save(ArtifactsDir + "FontSettings.TableSubstitutionRule.Windows.xml");

// Linux hat seine eigene Substitutionstabelle.
// Für „Times New Roman CE“ gibt es mehrere Ersatzschriften.
// Wenn der erste Ersatz „FreeSerif“ ebenfalls nicht verfügbar ist,
// Diese Regel durchläuft die anderen im Array, bis sie eine verfügbare Regel findet.
tableSubstitutionRule.LoadLinuxSettings();
Assert.AreEqual(new[] {"FreeSerif", "Liberation Serif", "DejaVu Serif"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// Speichern Sie die Linux-Ersetzungstabelle in Form eines XML-Dokuments mithilfe eines Streams.
using (FileStream fileStream = new FileStream(ArtifactsDir + "FontSettings.TableSubstitutionRule.Linux.xml",
    FileMode.Create))
{
    tableSubstitutionRule.Save(fileStream);
}
```

### Siehe auch

* class [TableSubstitutionRule](../)
* namensraum [Aspose.Words.Fonts](../../tablesubstitutionrule/)
* Montage [Aspose.Words](../../../)

---

## Save(Stream) {#save}

Speichert die aktuellen Tabellenersetzungseinstellungen im Stream.

```csharp
public void Save(Stream outputStream)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| outputStream | Stream | Ausgabestrom. |

### Beispiele

Zeigt, wie man auf Schriftarten-Ersetzungstabellen für Windows und Linux zugreift.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Erstellen Sie eine neue Tabellenersetzungsregel und laden Sie die Standard-Schriftartenersetzungstabelle von Microsoft Windows.
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;
tableSubstitutionRule.LoadWindowsSettings();

// In Windows ist der Standardersatz für die Schriftart „Times New Roman CE“ „Times New Roman“.
Assert.AreEqual(new[] {"Times New Roman"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// Wir können die Tabelle in Form eines XML-Dokuments speichern.
tableSubstitutionRule.Save(ArtifactsDir + "FontSettings.TableSubstitutionRule.Windows.xml");

// Linux hat seine eigene Substitutionstabelle.
// Für „Times New Roman CE“ gibt es mehrere Ersatzschriften.
// Wenn der erste Ersatz „FreeSerif“ ebenfalls nicht verfügbar ist,
// Diese Regel durchläuft die anderen im Array, bis sie eine verfügbare Regel findet.
tableSubstitutionRule.LoadLinuxSettings();
Assert.AreEqual(new[] {"FreeSerif", "Liberation Serif", "DejaVu Serif"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// Speichern Sie die Linux-Ersetzungstabelle in Form eines XML-Dokuments mithilfe eines Streams.
using (FileStream fileStream = new FileStream(ArtifactsDir + "FontSettings.TableSubstitutionRule.Linux.xml",
    FileMode.Create))
{
    tableSubstitutionRule.Save(fileStream);
}
```

### Siehe auch

* class [TableSubstitutionRule](../)
* namensraum [Aspose.Words.Fonts](../../tablesubstitutionrule/)
* Montage [Aspose.Words](../../../)


