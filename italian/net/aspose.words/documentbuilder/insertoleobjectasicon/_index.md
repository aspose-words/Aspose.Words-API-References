---
title: DocumentBuilder.InsertOleObjectAsIcon
linktitle: InsertOleObjectAsIcon
articleTitle: InsertOleObjectAsIcon
second_title: Aspose.Words per .NET
description: DocumentBuilder InsertOleObjectAsIcon metodo. Inserisce un oggetto OLE incorporato o collegato come icona nel documento. Permette di specificare il file dellicona e la didascalia. Rileva il tipo di oggetto OLE utilizzando lestensione file in C#.
type: docs
weight: 400
url: /it/net/aspose.words/documentbuilder/insertoleobjectasicon/
---
## InsertOleObjectAsIcon(*string, bool, string, string*) {#insertoleobjectasicon_1}

Inserisce un oggetto OLE incorporato o collegato come icona nel documento. Permette di specificare il file dell'icona e la didascalia. Rileva il tipo di oggetto OLE utilizzando l'estensione file.

```csharp
public Shape InsertOleObjectAsIcon(string fileName, bool isLinked, string iconFile, 
    string iconCaption)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fileName | String | Percorso completo del file. |
| isLinked | Boolean | Se`VERO` quindi viene inserito l'oggetto OLE collegato altrimenti viene inserito l'oggetto OLE incorporato. |
| iconFile | String | Percorso completo del file ICO. Se il valore è`nullo` , Aspose.Words utilizzerà un'immagine predefinita. |
| iconCaption | String | Didascalia dell'icona. Se il valore è`nullo` , Aspose.Words utilizzerà il nome file. |

### Valore di ritorno

Nodo forma contenente l'oggetto Ole e inserito nella posizione corrente del Builder.

## Esempi

Mostra come inserire un oggetto OLE in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Gli oggetti OLE sono collegamenti a file nel nostro file system locale che possono essere aperti da altre applicazioni installate.
// Facendo doppio clic su queste forme verrà avviata l'applicazione, quindi la utilizzerà per aprire l'oggetto collegato.
// Esistono tre modi per utilizzare il metodo InsertOleObject per inserire queste forme e configurarne l'aspetto.
// 1 - Immagine presa dal file system locale:
using (FileStream imageStream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
{
    // Se 'presentation' viene omesso ed è impostato 'asIcon', viene selezionato questo metodo sovraccaricato
    // l'icona in base all'estensione del file e utilizza il nome del file per la didascalia dell'icona.
    builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", false, false, imageStream); 
}

// Se 'presentation' viene omesso ed è impostato 'asIcon', viene selezionato questo metodo sovraccaricato
// l'icona in base a 'progId' e utilizza il nome file per la didascalia dell'icona.
// 2 - Icona in base all'applicazione che aprirà l'oggetto:
builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

// Se 'iconFile' e 'iconCaption' vengono omessi, questo metodo sovraccaricato seleziona
// l'icona in base a "progId" e utilizza la didascalia dell'icona predefinita.
// 3 - Icona immagine di 32 x 32 pixel o inferiore proveniente dal file system locale, con una didascalia personalizzata:
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", false, ImageDir + "Logo icon.ico",
    "Double click to view presentation!");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObject.docx");
```

### Guarda anche

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## InsertOleObjectAsIcon(*string, string, bool, string, string*) {#insertoleobjectasicon_2}

Inserisce un oggetto OLE incorporato o collegato come icona nel documento. Permette di specificare il file dell'icona e la didascalia. Rileva il tipo di oggetto OLE utilizzando il parametro progID specificato.

```csharp
public Shape InsertOleObjectAsIcon(string fileName, string progId, bool isLinked, string iconFile, 
    string iconCaption)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fileName | String | Percorso completo del file. |
| progId | String | ProgId dell'oggetto OLE. |
| isLinked | Boolean | Se`VERO` quindi viene inserito l'oggetto OLE collegato altrimenti viene inserito l'oggetto OLE incorporato. |
| iconFile | String | Percorso completo del file ICO. Se il valore è`nullo` , Aspose.Words utilizzerà un'immagine predefinita. |
| iconCaption | String | Didascalia dell'icona. Se il valore è`nullo` , Aspose.Words utilizzerà il nome file. |

### Valore di ritorno

Nodo forma contenente l'oggetto Ole e inserito nella posizione corrente del Builder.

## Esempi

Mostra come inserire un oggetto OLE incorporato o collegato come icona nel documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Se 'iconFile' e 'iconCaption' vengono omessi, questo metodo sovraccaricato seleziona
// l'icona in base a 'progId' e utilizza il nome file per la didascalia dell'icona.
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", "Package", false, ImageDir + "Logo icon.ico", "My embedded file");

builder.InsertBreak(BreakType.LineBreak);

using (FileStream stream = new FileStream(MyDir + "Presentation.pptx", FileMode.Open))
{
    // Se 'iconFile' e 'iconCaption' vengono omessi, questo metodo sovraccaricato seleziona
    // l'icona in base all'estensione del file e utilizza il nome del file per la didascalia dell'icona.
    Shape shape = builder.InsertOleObjectAsIcon(stream, "PowerPoint.Application", ImageDir + "Logo icon.ico",
        "My embedded file stream");

    OlePackage setOlePackage = shape.OleFormat.OlePackage;
    setOlePackage.FileName = "Presentation.pptx";
    setOlePackage.DisplayName = "Presentation.pptx";
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObjectAsIcon.docx");
```

### Guarda anche

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## InsertOleObjectAsIcon(*Stream, string, string, string*) {#insertoleobjectasicon}

Inserisce un oggetto OLE incorporato come icona da uno stream nel documento. Permette di specificare il file dell'icona e la didascalia. Rileva il tipo di oggetto OLE utilizzando il parametro progID specificato.

```csharp
public Shape InsertOleObjectAsIcon(Stream stream, string progId, string iconFile, 
    string iconCaption)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| stream | Stream | Stream contenente i dati dell'applicazione. |
| progId | String | ProgId dell'oggetto OLE. |
| iconFile | String | Percorso completo del file ICO. Se il valore è`nullo` , Aspose.Words utilizzerà un'immagine predefinita. |
| iconCaption | String | Didascalia dell'icona. Se il valore è`nullo` , Aspose.Words utilizzerà la didascalia di un'icona predefinita. |

### Valore di ritorno

Nodo forma contenente l'oggetto Ole e inserito nella posizione corrente del Builder.

## Esempi

Mostra come inserire un oggetto OLE incorporato o collegato come icona nel documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Se 'iconFile' e 'iconCaption' vengono omessi, questo metodo sovraccaricato seleziona
// l'icona in base a 'progId' e utilizza il nome file per la didascalia dell'icona.
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", "Package", false, ImageDir + "Logo icon.ico", "My embedded file");

builder.InsertBreak(BreakType.LineBreak);

using (FileStream stream = new FileStream(MyDir + "Presentation.pptx", FileMode.Open))
{
    // Se 'iconFile' e 'iconCaption' vengono omessi, questo metodo sovraccaricato seleziona
    // l'icona in base all'estensione del file e utilizza il nome del file per la didascalia dell'icona.
    Shape shape = builder.InsertOleObjectAsIcon(stream, "PowerPoint.Application", ImageDir + "Logo icon.ico",
        "My embedded file stream");

    OlePackage setOlePackage = shape.OleFormat.OlePackage;
    setOlePackage.FileName = "Presentation.pptx";
    setOlePackage.DisplayName = "Presentation.pptx";
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObjectAsIcon.docx");
```

### Guarda anche

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
