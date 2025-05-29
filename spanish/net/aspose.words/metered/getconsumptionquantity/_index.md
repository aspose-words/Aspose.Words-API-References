---
title: Metered.GetConsumptionQuantity
linktitle: GetConsumptionQuantity
articleTitle: GetConsumptionQuantity
second_title: Aspose.Words para .NET
description: Descubra el método GetConsumptionQuantity medido para recuperar eficientemente datos de tamaño de archivo y optimizar la gestión de recursos. ¡Mejore la información de sus datos!
type: docs
weight: 50
url: /es/net/aspose.words/metered/getconsumptionquantity/
---
## Metered.GetConsumptionQuantity method

Obtiene el tamaño del archivo de consumo

```csharp
public static decimal GetConsumptionQuantity()
```

### Valor_devuelto

cantidad de consumo

## Ejemplos

Muestra cómo activar una licencia medida y realizar un seguimiento del crédito/consumo.

```csharp
// Cree una nueva licencia medida y luego imprima sus estadísticas de uso.
Metered metered = new Metered();
metered.SetMeteredKey("MyPublicKey", "MyPrivateKey");

Console.WriteLine($"Is metered license accepted: {Metered.IsMeteredLicensed()}");
Console.WriteLine($"Product name: {metered.GetProductName()}");
Console.WriteLine($"Credit before operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity before operation: {Metered.GetConsumptionQuantity()}");

// Opere utilizando Aspose.Words y luego imprima nuevamente nuestras estadísticas medidas para ver cuánto gastamos.
Document doc = new Document(MyDir + "Document.docx");
doc.Save(ArtifactsDir + "Metered.Usage.pdf");

// El mecanismo de licencias medidas de Aspose no envía los datos de uso al servidor de compra cada vez,
// necesitas usar espera.
System.Threading.Thread.Sleep(10000);

Console.WriteLine($"Credit after operation: {Metered.GetConsumptionCredit()}");
Console.WriteLine($"Consumption quantity after operation: {Metered.GetConsumptionQuantity()}");
```

### Ver también

* class [Metered](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
