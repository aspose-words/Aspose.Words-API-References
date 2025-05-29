---
title: Metered.SetMeteredKey
linktitle: SetMeteredKey
articleTitle: SetMeteredKey
second_title: Aspose.Words para .NET
description: Gestione fácilmente su licencia medida con el método SetMeteredKey. Asegúrese de que la carga de datos sea fluida y evite el estado de evaluación con comprobaciones periódicas.
type: docs
weight: 30
url: /es/net/aspose.words/metered/setmeteredkey/
---
## Metered.SetMeteredKey method

Establece claves públicas y privadas medidas. Si compra una licencia medida, al iniciar la aplicación, se debe llamar a esta API; normalmente, esto es suficiente. Sin embargo, si siempre no se pueden cargar los datos de consumo y exceden las 24 horas, la licencia se establecerá en estado de evaluación. Para evitar tal caso, debe verificar regularmente el estado de la licencia; si está en estado de evaluación, vuelva a llamar a esta API.

```csharp
public void SetMeteredKey(string publicKey, string privateKey)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| publicKey | String | clave pública |
| privateKey | String | clave privada |

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
