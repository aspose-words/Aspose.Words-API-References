---
title: TableSubstitutionRule.LoadLinuxSettings
linktitle: LoadLinuxSettings
articleTitle: LoadLinuxSettings
second_title: Aspose.Words per .NET
description: Carica senza sforzo le impostazioni predefinite di sostituzione delle tabelle per Linux con il metodo LoadLinuxSettings. Ottimizza il tuo flusso di lavoro oggi stesso!
type: docs
weight: 50
url: /it/net/aspose.words.fonts/tablesubstitutionrule/loadlinuxsettings/
---
## TableSubstitutionRule.LoadLinuxSettings method

Carica le impostazioni predefinite di sostituzione delle tabelle per la piattaforma Linux.

```csharp
public void LoadLinuxSettings()
```

## Esempi

Mostra come accedere alle tabelle di sostituzione dei font per Windows e Linux.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Crea una nuova regola di sostituzione tabella e carica la tabella di sostituzione font predefinita di Microsoft Windows.
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;
tableSubstitutionRule.LoadWindowsSettings();

// In Windows, il sostituto predefinito del font "Times New Roman CE" è "Times New Roman".
Assert.AreEqual(new[] {"Times New Roman"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// Possiamo salvare la tabella sotto forma di documento XML.
tableSubstitutionRule.Save(ArtifactsDir + "FontSettings.TableSubstitutionRule.Windows.xml");

// Linux ha la sua tabella di sostituzione.
// Esistono diversi font sostitutivi per "Times New Roman CE".
// Se anche il primo sostituto, "FreeSerif", non è disponibile,
// questa regola scorrerà le altre nell'array finché non ne troverà una disponibile.
tableSubstitutionRule.LoadLinuxSettings();
Assert.AreEqual(new[] {"FreeSerif", "Liberation Serif", "DejaVu Serif"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// Salva la tabella di sostituzione di Linux sotto forma di documento XML utilizzando un flusso.
using (FileStream fileStream = new FileStream(ArtifactsDir + "FontSettings.TableSubstitutionRule.Linux.xml",
    FileMode.Create))
{
    tableSubstitutionRule.Save(fileStream);
}
```

### Guarda anche

* class [TableSubstitutionRule](../)
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
