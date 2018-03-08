# API

<!-- TOC -->

- [API](#api)
    - [Acceso](#acceso)
        - [Autenticaci&oacute;n](#autenticacioacuten)
    - [1 Stock](#1-stock)
        - [1.1 Petici&oacute;n](#11-peticioacuten)
            - [1.1.1 Par&aacute;metros URL](#111-paraacutemetros-url)
            - [1.1.1 Encabezado](#111-encabezado)
        - [1.2 Respuesta](#12-respuesta)
    - [2 Listas de Precios](#2-listas-de-precios)
        - [2.1 Petici&oacute;n](#21-peticioacuten)
            - [2.1.1 Par&aacute;metros URL](#211-paraacutemetros-url)
            - [2.1.2 Encabezado](#212-encabezado)
        - [2.2 Respuesta](#22-respuesta)
    - [3 Lista de Precios](#3-lista-de-precios)
        - [3.1 Petici&oacute;n](#31-peticioacuten)
            - [3.1.1 Par&aacute;metros URL](#311-paraacutemetros-url)
            - [3.1.2 Encabezado](#312-encabezado)
        - [3.2 Respuesta](#32-respuesta)
    - [4 Nuevo Pedido](#4-nuevo-pedido)
        - [4.1 Petici&oacute;n](#41-peticioacuten)
            - [4.1.1 Par&aacute;metros BODY](#411-paraacutemetros-body)
            - [4.1.2 Encabezado](#412-encabezado)
        - [4.2 Respuesta](#42-respuesta)
    - [5 Lista de Dep&oacute;sitos](#5-lista-de-depoacutesitos)
        - [5.1 Petici&oacute;n](#51-peticioacuten)
            - [5.1.1 Par&aacute;metros URL](#511-paraacutemetros-url)
            - [5.1.2 Encabezado](#512-encabezado)
        - [5.2 Respuesta](#52-respuesta)
    - [6 Lista de Paises](#6-lista-de-paises)
        - [6.1 Petici&oacute;n](#61-peticioacuten)
            - [6.1.1 Par&aacute;metros URL](#611-paraacutemetros-url)
            - [6.1.2 Encabezado](#612-encabezado)
        - [6.2 Respuesta](#62-respuesta)
    - [7 Lista de Provincias](#7-lista-de-provincias)
        - [7.1 Petici&oacute;n](#71-peticioacuten)
            - [7.1.1 Par&aacute;metros URL](#711-paraacutemetros-url)
            - [7.1.2 Encabezado](#712-encabezado)
        - [7.2 Respuesta](#72-respuesta)
    - [8 Lista de Clientes](#8-lista-de-clientes)
        - [8.1 Petici&oacute;n](#81-peticioacuten)
            - [8.1.1 Par&aacute;metros URL](#811-paraacutemetros-url)
            - [8.1.2 Encabezado](#812-encabezado)
        - [8.2 Respuesta](#82-respuesta)
    - [9 Lista de Vendedores](#9-lista-de-vendedores)
        - [9.1 Petici&oacute;n](#91-peticioacuten)
            - [9.1.1 Par&aacute;metros URL](#911-paraacutemetros-url)
            - [9.1.2 Encabezado](#912-encabezado)
        - [9.2 Respuesta](#92-respuesta)
    - [10 Lista de Art&iacute;culos](#10-lista-de-artiacuteculos)
        - [10.1 Petici&oacute;n](#101-peticioacuten)
            - [10.1.1 Par&aacute;metros URL](#1011-paraacutemetros-url)
            - [10.1.2 Encabezado](#1012-encabezado)
        - [10.2 Respuesta](#102-respuesta)
    - [11 Lista de Tarjetas o Modos de pago](#11-lista-de-tarjetas-o-modos-de-pago)
        - [11.1 Petici&oacute;n](#111-peticioacuten)
            - [11.1.1 Par&aacute;metros URL](#1111-paraacutemetros-url)
            - [11.1.2 Encabezado](#1112-encabezado)
        - [11.2 Respuesta](#112-respuesta)
    - [12 Planes](#12-planes)
        - [12.1 Petici&oacute;n](#121-peticioacuten)
            - [12.1.1 Par&aacute;metros URL](#1211-paraacutemetros-url)
            - [12.1.2 Encabezado](#1212-encabezado)
        - [12.2 Respuesta](#122-respuesta)
    - [13 Nuevo Cliente](#13-nuevo-cliente)
        - [13.1 Petici&oacute;n](#131-peticioacuten)
            - [13.1.1 Par&aacute;metros BODY](#1311-paraacutemetros-body)
            - [13.1.2 Encabezado](#1312-encabezado)
        - [13.2 Respuesta](#132-respuesta)

<!-- /TOC -->

## Acceso

### Autenticaci&oacute;n

La autenticaci&oacute;n se realizar&aacute; utilizando [JWT](https://jwt.io/) (Autenticaci&oacute;n basada en TOKENS).
JWT es un standard abierto ([RFC 7519](https://tools.ietf.org/html/rfc7519)) que autentica peticiones HTTP sin la necesidad de enviar en cada una de ellas las credenciales del usuario.

Es un mecanismo de Autenticaci&oacute;n y Autorizaci&oacute;n, no otorga ning&uacute;n tipo de privacidad en la comunicaci&oacute;n.

En el encabezado de cada petici&oacute;n se deber&aacute;n incluir estos par&aacute;metros:

> **X-APP-ID**: d852f92d887c3788efb8c08c38788969
>
> **X-TOKEN**: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM5MDIyfQ.XbPfbIHMI6arZ3Y922BhjWgQzWXcXNrz0ogtVhfEd2o
>
> **Content-Type**: appication/json

*X-APP-ID* Identificador de la aplicaci&oacute;n que sera provisto

*X-TOKEN* deer&aacute; ser obtenido mediante alguna de las librer&iacute;as disponibles en [JWT](https://jwt.io/).

## 1 Stock

### 1.1 Petici&oacute;n

> GET `/api/items/stock/?artd=[integer]&arth=[integer]&lstdep=[integer]│...│[integer]`

#### 1.1.1 Par&aacute;metros URL

| Par&aacute;metro|Tipo|Descripci&oacute;n|Obligatorio|
| -------------|-|-------------|:-----:|
| _artd_|int|c&oacute;digo art&iacute;culo desde|NO|
| _arth_|int|c&oacute;digo art&iacute;culo hasta|NO|
| _lstdep_|string|lista de codigos de dep&oacute;sitos separados por "│" (pipe)|NO|

#### 1.1.1 Encabezado

> **X-APP-ID**: d852f92d887c3788efb8c08c38788969
>
> **X-TOKEN**: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM5MDIyfQ.XbPfbIHMI6arZ3Y922BhjWgQzWXcXNrz0ogtVhfEd2o
>
> **Content-Type**: appication/json

### 1.2 Respuesta

**C&oacute;digo:**
> 200

**Contenido:**

>```json
>    [
>        {
>            "cod_articu" : "0200200065",
>            "cod_deposi" : "01",
>            "OnHand" : 100,
>            "SO" : 50,
>            "PO" : 30
>        },
>        {
>            "cod_articu" : "0100100134",
>            "cod_deposi" : "01",
>            "OnHand" : "150",
>            "SO" : 12,
>            "PO" : 0
>        }
>    ]
>```

**C&oacute;digo:**
> 404

**Contenido:**

>```json
>    {
>        "error" : "Artículos no encontrados"
>    }
>```

## 2 Listas de Precios

### 2.1 Petici&oacute;n

> GET `/api/items/listprices?nrolista=[integer]`

#### 2.1.1 Par&aacute;metros URL

| Par&aacute;metro|Tipo|Descripci&oacute;n|Obligatorio|
| ------------- | -|-------------|:-----:|
| _nrolista_|int|N&uacute;mero de lista|SI|

#### 2.1.2 Encabezado

> **X-APP-ID**: d852f92d887c3788efb8c08c38788969
>
> **X-TOKEN**: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM5MDIyfQ.XbPfbIHMI6arZ3Y922BhjWgQzWXcXNrz0ogtVhfEd2o
>
> **Content-Type**: appication/json

### 2.2 Respuesta

**C&oacute;digo:**
> 200

**Contenido:**

>```json
>    [
>        {
>            "nroLista" : 1,
>            "nombre" : "Venta Mayorista",
>            "monCte" : 1,
>            "incluyeIVA" : 0,
>            "desde" : "DD/MM/YYYY",
>            "hasta" : "DD/MM/YYYY"
>        },
>        {
>            "nroLista" : 5,
>            "nombre" : "Venta Minorista",
>            "monCte" : 1,
>            "incluyeIVA" : 1,
>            "desde" : "DD/MM/YYYY",
>            "hasta" : "DD/MM/YYYY"
>        }
>    ]
>```

**C&oacute;digo:**
> 404

**Contenido:**

>```json
>    {
>        "error" : "La lista no existe"
>    }
>```

## 3 Lista de Precios

### 3.1 Petici&oacute;n

> GET `/api/items/prices?nrolista=[integer]&fecd=[YYYYMMDD]`

#### 3.1.1 Par&aacute;metros URL

| Par&aacute;metro|Tipo|Descripci&oacute;n|Obligatorio|
| ------------- | -|-------------|:-----:|
| _nrolista_|int|N&uacute;mero de lista|SI|
| _fecd_|int|Fecha de &uacute;ltima modificaci&oacute;n|NO|

#### 3.1.2 Encabezado

> **X-APP-ID**: d852f92d887c3788efb8c08c38788969
>
> **X-TOKEN**: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM5MDIyfQ.XbPfbIHMI6arZ3Y922BhjWgQzWXcXNrz0ogtVhfEd2o
>
> **Content-Type**: appication/json

### 3.2 Respuesta

**C&oacute;digo:**
> 200

**Contenido:**

> ```json
>    [
>        {
>            "codart" : "0200200065",
>            "precio" : 4.3,
>            "base" : 0
>        },
>        {
>            "codart" : "0100100134",
>            "precio" : 3117.6,
>            "base" : 0
>        },
>    ]
>```

**C&oacute;digo:**
> 404

**Contenido:**

>```json
>    {
>        "error" : "La lista no existe"
>    }
>```

## 4 Nuevo Pedido

Inserta un nuevo pedido.

### 4.1 Petici&oacute;n

>POST `/api/order/`
>```
>defecto=[string]&cod_client=[int]&razon_soci=[string]&cuit=[string]&res_iva=[int]&domicilio=[string]&cod_provin=[string]&cod_transp=[string]&cod_zona=[int]&cod_vended=[int]&cond_vta=[int]&porc_dto=[int]
>```

#### 4.1.1 Par&aacute;metros BODY

| Par&aacute;metro|Tipo|Descripci&oacute;n|Obligatorio|
| -------------|-|-------------|:-----:|
| defecto| string| Plantilla modelo a utilizar| NO|
| cod_client| int|  C&oacute;digo de Cliente| NO|
| razon_soci| string| Raz&oacute;n Social| SI|
| cuit| string| CUIT| SI|
| res_iva| int| C&oacute;digo de situación ante el IVA| SI|
| domicilio| string| Domicilio| SI|
| cod_provin| string| C&oacute;digo de la Provincia| SI|
| cod_transp| string| C&oacute;digo de Transporte| NO|
| cod_zona| int| C&oacute;digo de la zona| SI|
| cod_vended| int| C&oacute;digo del vendendor| SI|
| cond_vta| int| C&oacute;digo de condición de venta| NO|
| porc_dto| int| Descuento a aplicar| NO|

#### 4.1.2 Encabezado

> **X-APP-ID**: d852f92d887c3788efb8c08c38788969
>
> **X-TOKEN**: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM5MDIyfQ.XbPfbIHMI6arZ3Y922BhjWgQzWXcXNrz0ogtVhfEd2o
>
> **Content-Type**: appication/json

### 4.2 Respuesta

**C&oacute;digo:**
> 200

**Contenido:**

>```json
>   {
>       "cod_pedido" : "R 0200200065",
>    }
>```

**C&oacute;digo:**
> 404

**Contenido:**

>```json
>    {
>        "error" : " @@@@@@@@@@@@@ no encontrados"
>    }
>```

## 5 Lista de Dep&oacute;sitos

### 5.1 Petici&oacute;n

> GET `/api/depos?coddep=[int]&nomdep=[string]&dirdep=[string]`

#### 5.1.1 Par&aacute;metros URL

| Par&aacute;metro|Tipo|Descripci&oacute;n|Obligatorio|
| ------------- | -|-------------|:-----:|
| _coddep_|int|C&oacute;digo de dep&oacute;sito|NO|
| _nomdep_|int|Nombre de dep&oacute;sito|NO|
| _dirdep_|string|Direcci&oacute;n de dep&oacute;sito|NO|

#### 5.1.2 Encabezado

> **X-APP-ID**: d852f92d887c3788efb8c08c38788969
>
> **X-TOKEN**: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM5MDIyfQ.XbPfbIHMI6arZ3Y922BhjWgQzWXcXNrz0ogtVhfEd2o
>
> **Content-Type**: appication/json

### 5.2 Respuesta

**C&oacute;digo:**
> 200

**Contenido:**

> ```json
>    [
>        {
>            "cod_deposi" : 5,
>            "nom_deposi" : "Ramirez",
>            "inhabilita" : 0,
>            "dir_deposi" : "Juan Ramirez 158",
>            "bastece" : 0,
>            "ucursal_destino" : 5,
>            "bservaciones" : "Sin comentarios"
>        },
>        {
>            "cod_deposi" : 7,
>            "nom_deposi" : "San Juan" ,
>            "inhabilita" : 0,
>            "dir_deposi" : "Avda San Martin 158",
>            "abastece" : 0,
>            "ucursal_destino" : 5,
>            "bservaciones" : "Sin comentarios"
>        }
>    ]
>```

**C&oacute;digo:**
> 404

**Contenido:**

>```json
>    {
>        "error" : "El dep&oacute;sito no existe"
>    }
>```

## 6 Lista de Paises

### 6.1 Petici&oacute;n

> GET `/api/country?codpais=[int]&nompais=[string]`

#### 6.1.1 Par&aacute;metros URL

| Par&aacute;metro|Tipo|Descripci&oacute;n|Obligatorio|
| ------------- | -|-------------|:-----:|
| _codpais_|int|C&oacute;digo de pais|NO|
| _nompais_|string|Nombre de pais|NO|

#### 6.1.2 Encabezado

> **X-APP-ID**: d852f92d887c3788efb8c08c38788969
>
> **X-TOKEN**: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM5MDIyfQ.XbPfbIHMI6arZ3Y922BhjWgQzWXcXNrz0ogtVhfEd2o
>
> **Content-Type**: appication/json

### 6.2 Respuesta

**C&oacute;digo:**
> 200

**Contenido:**

> ```json
>    [
>        {
>            "cod_pais" : 5,
>            "nom_pais" : "Argentina",
>            "od_afip" : 0
>        },
>        {
>            "cod_pais" : 6,
>            "nom_pais" : "Uruguay",
>            "cod_afip" : 0
>        }
>    ]
>```

**C&oacute;digo:**
> 404

**Contenido:**

>```json
>    {
>        "error" : "Pais no encontrado"
>    }
>```

## 7 Lista de Provincias

### 7.1 Petici&oacute;n

> GET `/api/province?codpcia=[string]&nompcia=[string]`

#### 7.1.1 Par&aacute;metros URL

| Par&aacute;metro|Tipo|Descripci&oacute;n|Obligatorio|
| ------------- | -|-------------|:-----:|
| _codpcia_|string|C&oacute;digo de provincia|NO|
| _nompcia_|string|Nombre de provincia|NO|

#### 7.1.2 Encabezado

> **X-APP-ID**: d852f92d887c3788efb8c08c38788969
>
> **X-TOKEN**: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM5MDIyfQ.XbPfbIHMI6arZ3Y922BhjWgQzWXcXNrz0ogtVhfEd2o
>
> **Content-Type**: appication/json

### 7.2 Respuesta

**C&oacute;digo:**
> 200

**Contenido:**

> ```json
>    [
>        {
>            "cod_pcia" : "05",
>            "nom_pcia" : "Buenos Aires"
>        },
>        {
>            "cod_pcia" : "06",
>            "nom_pcia" : "San Juan"
>        }
>    ]
>```

**C&oacute;digo:**
> 404

**Contenido:**

>```json
>    {
>       "error" : "Provincia no encontrado"
>    }
>```

## 8 Lista de Clientes

### 8.1 Petici&oacute;n

> GET `/api/client?codcli=[int]&nomcli=[string]&cuit=[string]`

#### 8.1.1 Par&aacute;metros URL

| Par&aacute;metro|Tipo|Descripci&oacute;n|Obligatorio|
| ------------- | -|-------------|:-----:|
| _codcli_|int|C&oacute;digo de cliente|NO|
| _nomcli_|string|Nombre de cliente|NO|
| _cuit_|string|CUIT de cliente|NO|

#### 8.1.2 Encabezado

> **X-APP-ID**: d852f92d887c3788efb8c08c38788969
>
> **X-TOKEN**: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM5MDIyfQ.XbPfbIHMI6arZ3Y922BhjWgQzWXcXNrz0ogtVhfEd2o
>
> **Content-Type**: appication/json

### 8.2 Respuesta

**C&oacute;digo:**
> 200

**Contenido:**

> ```json
>    [
>        {
>            "cod_client" : 5,
>            "nom_cliente" : "Buenos Aires",
>            "c_postal" : 3100,
>            "domicilio" : "Avda Ramirez 513",
>            "localidad" : "Buenos Aires",
>            "cod_provin" : "01",
>            "cod_transp" : "02",
>            "cod_vended" :25,
>            "cond_vta" : 1,
>            "nro_lista" : 7,
>            "cupo_credi" : 25000,
>            "observacio" : "Sin Comentarios",
>            "email" : "asdfasdf@asdfasdf.com",
>            "tipo_doc" : 80,
>            "cuit" : "20-29325757-1",
>            "fecha_inha" : "15/02/2017",
>            "iva_l" :"S",
>            "iva_d" :"N",
>            "porc_desc" :7.5,
>            "saldo_cc" : 7500
>        },
>        {
>            "cod_client" : 5,
>            "nom_cliente" : "Buenos Aires",
>            "c_postal" : 3100,
>            "domicilio" : "Avda San Martin 513",
>            "localidad" : "Buenos Aires",
>            "cod_provin" : "01",
>            "cod_transp" : "01",
>            "cod_vended" :25,
>            "cond_vta" : 1,
>            "nro_lista" : 7,
>            "cupo_credi" : 15000,
>            "observacio" : "Sin Comentarios",
>            "email" : "astresdf@asdfasdf.com",
>            "tipo_doc" : 80,
>            "cuit" : "20-28125957-1",
>            "fecha_inha" : "15/02/2017",
>            "iva_l" :"S",
>            "iva_d" :"N",
>            "porc_desc" :7.5,
>            "saldo_cc" : 7500
>        }
>    ]
>```

**C&oacute;digo:**
> 404

**Contenido:**

>```json
>    {
>        "error" : "Cliente no encontrado"
>    }
>```

## 9 Lista de Vendedores

### 9.1 Petici&oacute;n

> GET `/api/seller?codven=[int]&nomven=[string]`

#### 9.1.1 Par&aacute;metros URL

| Par&aacute;metro|Tipo|Descripci&oacute;n|Obligatorio|
| ------------- | -|-------------|:-----:|
| _codven_|int|C&oacute;digo de vendedor|NO|
| _nomven_|string|Nombre de vendedor|NO|

#### 9.1.2 Encabezado

> **X-APP-ID**: d852f92d887c3788efb8c08c38788969
>
> **X-TOKEN**: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM5MDIyfQ.XbPfbIHMI6arZ3Y922BhjWgQzWXcXNrz0ogtVhfEd2o
>
> **Content-Type**: appication/json

### 9.2 Respuesta

**C&oacute;digo:**
> 200

**Contenido:**

> ```json
>    [
>        {
>            "cod_vendedor" : 1,
>            "nom_vendedor" : "WALTER AREVALO",
>            "porc_comis" : 5
>        },
>        {
>            "cod_vendedor" : 2,
>            "nom_vendedor" : "ROSANA MONTEBLANCO",
>            "porc_comis" : 4
>        }
>    ]
>```

**C&oacute;digo:**
> 404

**Contenido:**

>```json
>    {
>        "error" : "Vendedor no encontrado"
>    }
>```

## 10 Lista de Art&iacute;culos

### 10.1 Petici&oacute;n

> GET `/api/items?codart=[int]&nomart=[string]`

#### 10.1.1 Par&aacute;metros URL

| Par&aacute;metro|Tipo|Descripci&oacute;n|Obligatorio|
| ------------- | -|-------------|:-----:|
| _codart_|string|C&oacute;digo de art&iacute;culo|NO|
| _nomart_|string|Nombre de art&iacute;culo|NO|

#### 10.1.2 Encabezado

> **X-APP-ID**: d852f92d887c3788efb8c08c38788969
>
> **X-TOKEN**: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM5MDIyfQ.XbPfbIHMI6arZ3Y922BhjWgQzWXcXNrz0ogtVhfEd2o
>
> **Content-Type**: appication/json

### 10.2 Respuesta

**C&oacute;digo:**
> 200

**Contenido:**

> ```json
>    [
>        {
>            "cod_articu" : "0200200298",
>            "descripcio" : "CHELADERA TROPICAL CFS",
>            "desc_adic" : "CON FREEZER SUPERIOR",
>            "sinonimo" : "HELTRO/FS",
>            "cod_barra" : "02468895631"
>        },
>        {
>            "cod_articu" : "0200200298",
>            "descripcio" : "LAVARROPAS AUTOMÁTICO MOD.EXCL",
>            "desc_adic" : "CON 19 PROGRAMAS",
>            "sinonimo" : "LVEXCELL",
>            "cod_barra" : "02468564320"
>        }
>    ]
>```

**C&oacute;digo:**
> 404

**Contenido:**

>```json
>    {
>        "error" : "Art&iacute;culo no encontrado"
>    }
>```

## 11 Lista de Tarjetas o Modos de pago

### 11.1 Petici&oacute;n

> GET `/api/cards?codtar=[string]`

#### 11.1.1 Par&aacute;metros URL

| Par&aacute;metro|Tipo|Descripci&oacute;n|Obligatorio|
| ------------- | -|-------------|:-----:|
| _codtar_|string|C&oacute;digo de tarjeta|NO|

#### 11.1.2 Encabezado

> **X-APP-ID**: d852f92d887c3788efb8c08c38788969
>
> **X-TOKEN**: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM5MDIyfQ.XbPfbIHMI6arZ3Y922BhjWgQzWXcXNrz0ogtVhfEd2o
>
> **Content-Type**: appication/json

### 11.2 Respuesta

**C&oacute;digo:**
> 200

**Contenido:**

> ```json
>    [
>        {
>            "cod_tarjeta" : "VI",
>            "nom_tarjeta" : "VISA",
>            "usa_pos" : 0,
>            "cupon_modo" : "M",
>            "redon_cuot" : "P",
>            "hora_cierre" : "18:00"
>        },
>        {
>            "cod_tarjeta" : "MC",
>            "nom_tarjeta" : "MASTERCARD",
>            "usa_pos" : 1,
>            "cupon_modo" : "",
>            "redon_cuot" : "P",
>            "hora_cierre" : "00:00"
>        }
>    ]
>```

**C&oacute;digo:**
> 404

**Contenido:**

>```json
>    {
>        "error" : "Tarjeta no encontrada"
>    }
>```

## 12 Planes

### 12.1 Petici&oacute;n

> GET `/api/cards?codtar=[string]&cuotas=[]`

#### 12.1.1 Par&aacute;metros URL

| Par&aacute;metro|Tipo|Descripci&oacute;n|Obligatorio|
| ------------- | -|-------------|:-----:|
| _codtar_|string|C&oacute;digo de tarjeta|NO|
| _cuotas_|int|Cantidad de cuotas|SI|

#### 12.1.2 Encabezado

> **X-APP-ID**: d852f92d887c3788efb8c08c38788969
>
> **X-TOKEN**: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM5MDIyfQ.XbPfbIHMI6arZ3Y922BhjWgQzWXcXNrz0ogtVhfEd2o
>
> **Content-Type**: appication/json

### 12.2 Respuesta

**C&oacute;digo:**
> 200

**Contenido:**

> ```json
>    [
>        {
>            "cod_tarjeta" : "VI",
>            "cuotas" : 1,
>            "plan" : "1 PAGO",
>            "comision" : "1.55",
>            "habitual" : 0,
>            "tipo_acre" : "D",
>            "plan_edi" : "E",
>            "cuotasmin" :1,
>            "porc_desc" :0.5
>        },
>        {
>            "cod_tarjeta" : "MC",
>            "cuotas" : 1,
>            "plan" : "1 PAGO",
>            "comision" : "1.25",
>            "habitual" : 0,
>            "tipo_acre" : "D",
>            "plan_edi" : "E",
>            "cuotasmin" :1,
>            "porc_desc" :0.75
>        }
>    ]
>```

**C&oacute;digo:**
> 404

**Contenido:**

>```json
>    {
>        "error" : "Plan no encontrado"
>    }
>```

## 13 Nuevo Cliente

Inserta un nuevo cliente.

### 13.1 Petici&oacute;n

>POST `/api/client/`
>```
>defecto=[string]&codcliauto=[string]&cod_client=[int]&habilitado=[string]&razon_soci=[string]&cuit=[string]&res_iva=[int]&domicilio=[string]
>```

#### 13.1.1 Par&aacute;metros BODY

| Par&aacute;metro|Tipo|Descripci&oacute;n|Obligatorio|
| -------------|-|-------------|:-----:|
| defecto| string| Plantilla modelo a utilizar| NO|
| codcliauto| string|  C&oacute;digo de Cliente| NO|
| cod_client| string|  C&oacute;digo de Cliente| NO|
| habilitado| string|  Cliente habilitado| NO|
| razon_soci| string| Raz&oacute;n Social| SI|
| cuit| string| CUIT| SI|
| res_iva| int| C&oacute;digo de situación ante el IVA| SI|
| domicilio| string| Domicilio| SI|

#### 13.1.2 Encabezado

> **X-APP-ID**: d852f92d887c3788efb8c08c38788969
>
> **X-TOKEN**: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM5MDIyfQ.XbPfbIHMI6arZ3Y922BhjWgQzWXcXNrz0ogtVhfEd2o
>
> **Content-Type**: appication/json

### 13.2 Respuesta

**C&oacute;digo:**
> 200

**Contenido:**

>```json
>   {
>       "resultado" : "<id>",
>   }
>```

**C&oacute;digo:**
> 404

**Contenido:**

>```json
>    {
>        "error" : "No se pudo dar de alta el cliente"
>    }
>```
