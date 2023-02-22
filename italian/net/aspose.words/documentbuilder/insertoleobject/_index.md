---
title: DocumentBuilder.InsertOleObject
second_title: Aspose.Words per .NET API Reference
description: DocumentBuilder metodo. Inserisce un oggetto OLE incorporato da un flusso nel documento.
type: docs
weight: 370
url: /it/net/aspose.words/documentbuilder/insertoleobject/
---
## InsertOleObject(Stream, string, bool, Stream) {#insertoleobject}

Inserisce un oggetto OLE incorporato da un flusso nel documento.

```csharp
public Shape InsertOleObject(Stream stream, string progId, bool asIcon, Stream presentation)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| stream | Stream | Stream contenente i dati dell'applicazione. |
| progId | String | Identificatore programmatico dell'oggetto OLE. |
| asIcon | Boolean | Specifica la modalità Iconica o Normale dell'oggetto OLE inserito. |
| presentation | Stream | Presentazione dell'immagine dell'oggetto OLE. Se il valore è null Aspose.Words utilizzerà una delle immagini predefinite. |

### Valore di ritorno

Nodo di forma contenente l'oggetto Ole e inserito nella posizione corrente del Builder.

### Esempi

Mostra come utilizzare il generatore di documenti per incorporare oggetti OLE in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisce un foglio di calcolo Microsoft Excel dal file system locale
// nel documento mantenendo il suo aspetto predefinito.
using (Stream spreadsheetStream = File.Open(MyDir + "Spreadsheet.xlsx", FileMode.Open))
{
    builder.Writeln("Spreadsheet Ole object:");
    // Se 'presentation' è omesso e 'asIcon' è impostato, questo metodo di overload seleziona
    // l'icona in base a 'progId' e utilizza la didascalia dell'icona predefinita.
    builder.InsertOleObject(spreadsheetStream, "OleObject.xlsx", false, null);
}

// Inserisce una presentazione Microsoft Powerpoint come oggetto OLE.
// Questa volta avrà un'immagine scaricata dal Web per un'icona.
using (Stream powerpointStream = File.Open(MyDir + "Presentation.pptx", FileMode.Open))
{
    using (WebClient webClient = new WebClient())
    {
        byte[] imgBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

        using (MemoryStream imageStream = new MemoryStream(imgBytes))
        {
            builder.InsertParagraph();
            builder.Writeln("Powerpoint Ole object:");
            builder.InsertOleObject(powerpointStream, "OleObject.pptx", true, imageStream);
        }
    }
}

// Fare doppio clic su questi oggetti in Microsoft Word per aprirli
// i file collegati utilizzando le rispettive applicazioni.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObjects.docx");
```

### Guarda anche

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../documentbuilder/)
* assemblea [Aspose.Words](../../../)

---

## InsertOleObject(string, bool, bool, Stream) {#insertoleobject_1}

Inserisce un oggetto OLE incorporato o collegato da un file nel documento. Rileva il tipo di oggetto OLE utilizzando l'estensione del file.

```csharp
public Shape InsertOleObject(string fileName, bool isLinked, bool asIcon, Stream presentation)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fileName | String | Percorso completo del file. |
| isLinked | Boolean | Se true, viene inserito l'oggetto OLE collegato, altrimenti viene inserito l'oggetto OLE incorporato. |
| asIcon | Boolean | Specifica la modalità Iconica o Normale dell'oggetto OLE inserito. |
| presentation | Stream | Presentazione dell'immagine dell'oggetto OLE. Se il valore è null Aspose.Words utilizzerà una delle immagini predefinite. |

### Valore di ritorno

Nodo di forma contenente l'oggetto Ole e inserito nella posizione corrente del Builder.

### Esempi

Mostra come inserire un oggetto OLE in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Gli oggetti OLE sono collegamenti a file nel nostro file system locale che possono essere aperti da altre applicazioni installate.
// Fare doppio clic su queste forme avvierà l'applicazione, quindi la utilizzerà per aprire l'oggetto collegato.
// Esistono tre modi per utilizzare il metodo InsertOleObject per inserire queste forme e configurarne l'aspetto.
// 1 - Immagine presa dal file system locale:
using (FileStream imageStream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
{
    // Se 'presentation' è omesso e 'asIcon' è impostato, questo metodo di overload seleziona
    // l'icona in base all'estensione del file e utilizza il nome del file per la didascalia dell'icona.
    builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", false, false, imageStream); 
}

// Se 'presentation' è omesso e 'asIcon' è impostato, questo metodo di overload seleziona
// l'icona in base a 'progId' e utilizza il nome del file per la didascalia dell'icona.
// 2 - Icona basata sull'applicazione che aprirà l'oggetto:
builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

// Se 'iconFile' e 'iconCaption' vengono omessi, viene selezionato questo metodo di overload
// l'icona in base a 'progId' e utilizza la didascalia dell'icona predefinita.
// 3 - Icona dell'immagine di 32 x 32 pixel o inferiore rispetto al file system locale, con una didascalia personalizzata:
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", false, ImageDir + "Logo icon.ico",
    "Double click to view presentation!");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObject.docx");
```

### Guarda anche

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../documentbuilder/)
* assemblea [Aspose.Words](../../../)

---

## InsertOleObject(string, string, bool, bool, Stream) {#insertoleobject_2}

Inserisce un oggetto OLE incorporato o collegato da un file nel documento. Rileva il tipo di oggetto OLE utilizzando il parametro progID specificato.

```csharp
public Shape InsertOleObject(string fileName, string progId, bool isLinked, bool asIcon, 
    Stream presentation)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fileName | String | Percorso completo del file. |
| progId | String | ProgId dell'oggetto OLE. |
| isLinked | Boolean | Se true, viene inserito l'oggetto OLE collegato, altrimenti viene inserito l'oggetto OLE incorporato. |
| asIcon | Boolean | Specifica la modalità Iconica o Normale dell'oggetto OLE inserito. |
| presentation | Stream | Presentazione dell'immagine dell'oggetto OLE. Se il valore è null Aspose.Words utilizzerà una delle immagini predefinite. |

### Valore di ritorno

Nodo di forma contenente l'oggetto Ole e inserito nella posizione corrente del Builder.

### Esempi

Mostra come inserire un oggetto OLE in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Gli oggetti OLE sono collegamenti a file nel nostro file system locale che possono essere aperti da altre applicazioni installate.
// Fare doppio clic su queste forme avvierà l'applicazione, quindi la utilizzerà per aprire l'oggetto collegato.
// Esistono tre modi per utilizzare il metodo InsertOleObject per inserire queste forme e configurarne l'aspetto.
// 1 - Immagine presa dal file system locale:
using (FileStream imageStream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
{
    // Se 'presentation' è omesso e 'asIcon' è impostato, questo metodo di overload seleziona
    // l'icona in base all'estensione del file e utilizza il nome del file per la didascalia dell'icona.
    builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", false, false, imageStream); 
}

// Se 'presentation' è omesso e 'asIcon' è impostato, questo metodo di overload seleziona
// l'icona in base a 'progId' e utilizza il nome del file per la didascalia dell'icona.
// 2 - Icona basata sull'applicazione che aprirà l'oggetto:
builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

// Se 'iconFile' e 'iconCaption' vengono omessi, viene selezionato questo metodo di overload
// l'icona in base a 'progId' e utilizza la didascalia dell'icona predefinita.
// 3 - Icona dell'immagine di 32 x 32 pixel o inferiore rispetto al file system locale, con una didascalia personalizzata:
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", false, ImageDir + "Logo icon.ico",
    "Double click to view presentation!");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObject.docx");
```

### Guarda anche

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../documentbuilder/)
* assemblea [Aspose.Words](../../../)


