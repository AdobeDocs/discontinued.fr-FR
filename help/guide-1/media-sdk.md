---
title: FAQ sur la fin de vie d’Adobe Analytics Media SDK (versions 1.x et 2.x)
description: Obtenez des réponses aux questions fréquentes sur la fin de vie des versions 1.x et 2.x d’Adobe Media SDK (anciennement la bibliothèque de pulsations vidéo).
source-git-commit: 4056ba0953e81a279d25b15449c7b41a4a5eb7f9
workflow-type: tm+mt
source-wordcount: '1051'
ht-degree: 1%
---

# FAQ sur la fin de vie d’Adobe Analytics Media SDK (versions 1.x et 2.x)

Adobe Media SDK **2.x a pris fin le 31 août 2021**. La prise en charge de la bibliothèque de pulsations vidéo (VHL) **1.x a pris fin le 25 juillet 2017**.

## Que se passe-t-il ?

La bibliothèque de pulsations vidéo d’origine (VHL), renommée par la suite Media SDK, fournissait un suivi côté client pour les analyses audio et vidéo. Adobe a migré les fonctionnalités de tracking vers des implémentations plus récentes et plus performantes :

* **Media SDK 3.x (Analytics uniquement) :** actuellement pris en charge. Effectue le suivi des médias à l’aide de l’API Media Collection. Recommandé pour les utilisateurs et utilisatrices 2.x qui ne peuvent pas encore migrer vers Edge Network.
* **Streaming Media for Edge Network (recommandé) :** implémentation actuellement recommandée. Utilise Adobe Experience Platform Web SDK, Mobile SDK ou l’API Media Edge pour envoyer des données multimédia via Edge Network, ce qui permet d’utiliser dans Adobe Analytics, Customer Journey Analytics, Real-Time CDP et Adobe Journey Optimizer.

## Qu’est-ce qui est inclus dans la fin de vie et qu’est-ce qui ne l’est pas ?

**Fin de vie (non prise en charge) :**

* Video Heartbeat Library (VHL) 1.x : toutes les plateformes (Android, iOS, JavaScript, Apple TV, Chromecast, Roku, TVML)
* Media SDK 2.x — Android, iOS, JavaScript

**Pas de fin de vie (toujours prise en charge) :**

* Media SDK 3.x - JavaScript, Chromecast, Roku (Analytics uniquement)
* Streaming Media for Edge Network - toutes les plateformes prises en charge

## Pourquoi les versions 1.x et 2.x ont-elles été retirées ?

À partir de la version 3.0, Media SDK a été repensé pour utiliser directement l’API Media Collection, ce qui élimine la nécessité d’un modèle de délégué et simplifie la création d’un outil de suivi. Les anciens SDK 1.x et 2.x reposaient sur une architecture de serveur Heartbeat qui a depuis été remplacée.

Adobe a également introduit la mise en œuvre d’Edge Network pour fournir un pipeline de collecte de données unique capable d’alimenter plusieurs applications Adobe en aval, ce que les SDK Heartbeat hérités ne pouvaient pas prendre en charge.

## Où trouver la documentation archivée ?

La documentation héritée a été archivée sur GitHub et est disponible pour référence :

| Version | Statut | Documentation archivée |
|---|---|---|
| 1.x (bibliothèque de pulsations vidéo) | Fin de la prise en charge le 25 juillet 2017 | [`video-heartbeat` référentiel GitHub](https://github.com/Adobe-Marketing-Cloud/video-heartbeat/tree/master/docs) |
| 2.x (Media SDK) | Fin de la prise en charge le 31 août 2021 | [`media-sdks` référentiel GitHub](https://github.com/Adobe-Marketing-Cloud/media-sdks/blob/master/docs/2.x/README.md) |

## Quelles sont mes options de transition ?

**Option 1 : Migrer vers Media SDK 3.x (Analytics uniquement)**

Si vous utilisez uniquement Adobe Analytics sur 2.x, la migration vers 3.x est le chemin le plus simple. Consultez le guide de migration [2.x vers 3.x](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/media-sdk/setup/migrate-js-2x-to-3x.html) pour une comparaison complète des API et des exemples de code.

**Option 2 : Migrer vers Streaming Media for Edge Network (recommandé)**

Pour les nouvelles mises en œuvre ou lorsque vous souhaitez utiliser des données dans plusieurs applications Adobe, utilisez l’Edge Network Adobe Experience Platform :

* [SDK Web Media Edge](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/edge/edge-web-sdk.html)
* [SDK Media Edge Mobile](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/edge/edge-mobile-sdk.html)
* [API Media Edge](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/edge/implementation-edge-api.html)

## Questions fréquentes

+++**La prise en charge des SDK Roku et Chromecast sera-t-elle affectée ?**

Non. Les SDK Roku et Chromecast restent disponibles et pris en charge dans le cadre de Media SDK 3.x (Analytics uniquement). Cette fin de vie ne concerne que les versions 1.x et 2.x.

+++

+++**Les implémentations de Media Analytics JavaScript SDK seront-elles affectées ?**

Non. Les clients qui utilisent JavaScript SDK for Media Analytics peuvent continuer à utiliser l’extension SDK ou de balise autonome.

+++

+++**Je suis toujours sur Media SDK 2.x. Que dois-je faire ?**

Adobe recommande de migrer vers l’implémentation d’Edge Network pour tous les nouveaux projets. Si vous avez besoin d’une étape intermédiaire, [Migrer de JavaScript SDK 2.x vers 3.x](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/media-sdk/setup/migrate-js-2x-to-3x.html), puis planifiez votre déplacement vers Edge Network.

+++

+++**Quel est le niveau d’effort pour migrer vers une implémentation prise en charge ?**

L’effort de migration dépend de l’implémentation de chaque client et varie. Après avoir consulté la documentation sur la migration, demandez conseil ou assistance clientèle pour une assistance supplémentaire :

* [Mise en œuvre de Streaming Media à l’aide de Mobile Edge SDK — Android et iOS](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/edge/edge-mobile-sdk.html)
* [Migration de JavaScript SDK 2.x vers 3.x](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/media-sdk/setup/migrate-js-2x-to-3x.html)

+++

+++**Dois-je utiliser Adobe Experience Platform Tags en tant que système de gestion des balises ?**

Pour les implémentations d’applications mobiles, Experience Platform Tags n’est pas utilisé comme système de gestion des balises, comme c’est le cas pour le web. L’interface utilisateur des balises est nécessaire pour configurer les extensions de SDK. Cette opération est similaire à la manière dont l’interface utilisateur d’Adobe Mobile Services a été utilisée pour configurer Mobile v4 SDK. Les balises fournissent des instructions d’installation personnalisées en fonction de l’extension de votre choix.

+++

+++**Cet abandon de la prise en charge a-t-il une incidence sur SDK pour tvOS ?**

Oui. Pour tvOS (version 10+), il est recommandé de migrer vers Streaming Media pour Edge Network à l’aide de Adobe Experience Platform Mobile SDK. Pour plus d’informations, consultez [&#x200B; Implémentation de Streaming Media à l’aide de Mobile Edge SDK &#x200B;](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/edge/edge-mobile-sdk.html).

+++

+++**Cet abandon de la prise en charge a-t-il une incidence sur SDK pour Fire TV et Android TV ?**

Oui. Pour Fire TV et Android TV, il est recommandé de migrer vers Streaming Media pour Edge Network à l’aide de Adobe Experience Platform Mobile SDK. Pour plus d’informations, consultez [&#x200B; Implémentation de Streaming Media à l’aide de Mobile Edge SDK &#x200B;](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/edge/edge-mobile-sdk.html).

+++

+++**Où puis-je trouver les informations de fin de vie du SDK Mobile v4 ?**

Voir la [FAQ sur la fin de vie de Mobile Services](mobile-services.md). La plateforme Mobile Services et les SDK Mobile v4 ont atteint leur fin de vie le 31 décembre 2022.

+++

+++**Où puis-je aller si j&#39;ai des questions ?**

Contactez votre équipe de compte Adobe ou l’assistance clientèle Adobe pour obtenir de l’aide sur la migration.

+++

>[!MORELIKETHIS]
>
>* [Présentation de l’implémentation de Streaming Media](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/overview.html)
>* [Streaming Media pour Edge Network](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/edge/implementation-edge.html)
>* [Media SDK 3.x — Configuration de JavaScript](https://experienceleague.adobe.com/docs/media-analytics/using/implementation/media-sdk/setup/web-implementation.html)
