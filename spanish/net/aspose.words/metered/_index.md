---
title: Metered Class
linktitle: Metered
articleTitle: Metered
second_title: Aspose.Words para .NET
description: Aspose.Words.Metered clase. Proporciona métodos para configurar la clave medida en C#.
type: docs
weight: 4160
url: /es/net/aspose.words/metered/
---
## Metered class

Proporciona métodos para configurar la clave medida.

Para obtener más información, visite el[Licencia y suscripción](https://docs.aspose.com/words/net/licensing/) artículo de documentación.

```csharp
public class Metered
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [Metered](metered/)() | Inicializa una nueva instancia de esta clase. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [SetMeteredKey](../../aspose.words/metered/setmeteredkey/)(*string, string*) | Establece la clave pública y privada medida. Si compra una licencia medida, cuando inicie la aplicación, se debe llamar a esta API; normalmente, esto es suficiente. Sin embargo, si siempre no se pueden cargar los datos de consumo y excede las 24 horas, la licencia se establecerá en estado de evaluación, para evitar tal caso, debe verificar periódicamente el estado de la licencia; si está en estado de evaluación, llame a esta API nuevamente. |
| static [GetConsumptionCredit](../../aspose.words/metered/getconsumptioncredit/)() | Obtiene crédito de consumo |
| static [GetConsumptionQuantity](../../aspose.words/metered/getconsumptionquantity/)() | Obtiene el tamaño del archivo de consumo |

## Ejemplos

En este ejemplo, se intentará establecer la clave pública y privada medida

```csharp
[C#]

Metered matered = new Metered();
matered.SetMeteredKey("PublicKey", "PrivateKey");


[Visual Basic]

Dim matered As Metered = New Metered
matered.SetMeteredKey("PublicKey", "PrivateKey")
```

Muestra cómo activar una licencia medida y realizar un seguimiento del crédito/consumo.

```csharp
// Cree una nueva licencia medida y luego imprima sus estadísticas de uso.
Metered metered = new Metered();
metered.SetMeteredKey("MyPublicKey", "MyPrivateKey");

Console.WriteLine($"Credit before operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity before operation: {Metered.GetConsumptionQuantity()}");

// Opere usando Aspose.Words y luego imprima nuestras estadísticas medidas nuevamente para ver cuánto gastamos.
Document doc = new Document(MyDir + "Document.docx");
doc.Save(ArtifactsDir + "Metered.Usage.pdf");

// El mecanismo de licencia medida de Aspose no envía los datos de uso al servidor de compra cada vez,
// necesitas usar la espera.
System.Threading.Thread.Sleep(10000);

Console.WriteLine($"Credit after operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity after operation: {Metered.GetConsumptionQuantity()}");
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
