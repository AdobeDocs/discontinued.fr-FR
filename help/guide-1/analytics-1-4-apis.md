---
title: Fin de vie de l’API Adobe Analytics 1.4
description: L’API Adobe Analytics 1.4 et l’authentification WSSE sont terminées le 31 août 2026. Découvrez ce qui est affecté et comment migrer vers les API Analytics 2.0.
source-git-commit: 4056ba0953e81a279d25b15449c7b41a4a5eb7f9
workflow-type: tm+mt
source-wordcount: '743'
ht-degree: 1%
---
# Fin de vie de l’API Adobe Analytics 1.4

Depuis **le 31 août 2026** Adobe a supprimé l’API Adobe Analytics 1.4 et l’authentification WSSE. Tous les points d’entrée qui utilisent cette version de l’API ne sont plus accessibles et les intégrations reposant sur celle-ci ont cessé de fonctionner.

Les API d’Adobe Analytics 1.4 fournissaient un large éventail d’actions, telles que la création de rapports, les classifications, les flux de données, les segments, les mesures calculées, les sources de données et la configuration des suites de rapports. Ils ont été remplacés par les [API Adobe Analytics 2.0](https://developer.adobe.com/analytics-apis/docs/2.0), qui vous permettent d’effectuer pratiquement toutes les actions disponibles dans l’interface utilisateur d’Adobe Analytics, y compris la création de rapports et la gestion de composants tels que les segments et les mesures calculées. Si vous disposez d’une intégration qui doit encore être mise à niveau, suivez le guide relatif à la [Migration vers les API Adobe Analytics 2.0](https://developer.adobe.com/analytics-apis/docs/2.0/guides/migration).

## Ce qui a atteint la fin de vie

Cette fin de vie a un impact direct sur les fonctionnalités d’API 1.4 suivantes. Migrez chaque workflow affecté vers les [API Adobe Analytics 2.0](https://developer.adobe.com/analytics-apis/docs/2.0) :

* Reporting (y compris les rapports Data Warehouse, en temps réel, de cheminement et de synthèse)
* Configuration et administration des suites de rapports
* Classifications
* Segments
* Mesures calculées
* Sources de données
* Flux de données
* Signets et méthodes de la société (point d’entrée)

Il annule également l’**authentification WSSE d’** (voir [Authentification WSSE](#wsse-authentication) ci-dessous).

>[!IMPORTANT]
>
>Cette fin de vie n’affecte *pas* votre collecte de données. Les solutions de balisage telles que Tags (anciennement Adobe Launch), Web SDK et AppMeasurement ne sont pas affectées. Le [API Data Insertion](#data-insertion-api) est également *non* retiré. Cependant, si vous utilisez les API Data Sources ou Classifications de la version 1.4 pour améliorer vos données, vous devez migrer ces workflows vers les API Adobe Analytics 2.0.

## Authentification WSSE

L’authentification WSSE est un protocole d’authentification hérité pris en charge par les API Analytics 1.4. Il a été remplacé par les options d’authentification basées sur OAuth fournies dans [&#128279;](https://developer.adobe.com/console/home). Les projets qui utilisaient l’authentification WSSE doivent mettre à jour leurs informations d’identification vers celles configurées dans le Adobe Developer Console.

Pour migrer, connectez-vous à [&#128279;](https://developer.adobe.com/console/home) et créez un projet pour votre intégration de l’API Analytics 2.0. Sélectionnez la méthode d’authentification **Utilisateur OAuth** ou **Serveur à serveur OAuth**.

## API d’insertion de données

L’API Data Insertion ne fait **pas** partie de cette fin de vie. Sa documentation a été déplacée vers le site [API de collecte de données &#x200B;](https://developer.adobe.com/analytics-collection-apis/) avec les autres méthodes de collecte côté serveur :

* [API Data Insertion](https://developer.adobe.com/analytics-collection-apis/methods/data-insertion/) : envoyez des données d’événement un accès à la fois, sous la forme d’une chaîne de requête (demande d’image) ou d’un `POST` XML.
* [API Bulk Data Insertion](https://developer.adobe.com/analytics-collection-apis/methods/bulk-data-insertion/) : chargez des lots de données d’appels au serveur sous forme de fichiers. Adobe recommande d’utiliser l’API Bulk Data Insertion pour les nouvelles implémentations côté serveur.

## Forum aux questions

+++Cela a-t-il un impact sur mes projets Adobe Developer existants pour les API Analytics ?

Tous les projets existants qui utilisent les API Analytics 1.4 sont affectés. Ces intégrations doivent être migrées vers les API [Adobe Analytics 2.0](https://developer.adobe.com/analytics-apis/docs/2.0/).

+++

+++J’ai partagé mes informations d’identification Adobe avec un autre produit ou une autre application qui utilise les API Analytics. Sont-ils touchés ?

Si ce produit ou cette application utilise vos informations d’identification WSSE ou appelle les API Analytics 1.4, ils sont affectés et doivent migrer. Contactez le fournisseur du produit ou de l’application pour obtenir plus d’informations sur ses plans de migration et son calendrier.

+++

+++Comment puis-je déterminer l’API utilisée par mon projet ?

L’URL de base que votre projet appelle détermine la version d’API qu’il utilise. Les API d’Adobe Analytics 1.4 utilisaient les URL de base suivantes :

* `https://api.omniture.com`
* `https://api3.omniture.com`
* `https://api4.omniture.com`
* `https://api5.omniture.com`

Les API [Adobe Analytics 2.0](https://developer.adobe.com/analytics-apis/docs/2.0/) utilisent l’URL de base suivante :

* `https://analytics.adobe.io`

Si l’un de vos projets d’API appelle `api*.omniture.com`, il utilise les API Adobe Analytics 1.4 retirées et doit migrer vers les API 2.0.

+++

+++Cette fin de vie a-t-elle une incidence sur la collecte de données ?

Non. Cette fin de vie n’a **pas** d’incidence sur la collecte directe de données, telles que les balises, le SDK web, AppMeasurement ou l’API Data Insertion. Cependant, si vous utilisez les API Data Sources ou Classifications de la version 1.4 pour améliorer vos données, vous devez migrer ces workflows vers les API Adobe Analytics 2.0.

+++

Si vous avez d’autres questions sur cette fin de vie auxquelles aucune réponse ne figure sur cette page, contactez l’équipe chargée de votre compte Adobe.
