---
keywords: Device-graph;fin de vie
title: Graphique de l’appareil
description: Découvrez les plans de fin de vie du graphique Appareil .
hold: true
source-git-commit: 0ebe153e886f375683ff3fc3a06514617988894b
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 4%

---

# Fin de vie du graphique d’appareil

>[!WARNING]
>
>Le graphique d’appareil dans les analyses entre appareils n’est plus disponible à compter du **31 décembre 2025**. Veuillez basculer n’importe quelle suite de rapports virtuelle actuellement activée pour les graphiques d’appareils vers la méthode [&#x200B; basée sur les champs](https://experienceleague.adobe.com/en/docs/analytics/components/cda/field-based-stitching).

Analytics sur l’ensemble des appareils a utilisé le graphique privé pour regrouper les données. Le graphique privé est un référentiel d’identifiants d’appareil hachés, spécifique à votre organisation. Analytics sur l’ensemble des appareils communique régulièrement avec le graphique des appareils pour lier les appareils.

## Conditions préalables spécifiques au graphique de l’appareil

Si vous aviez l’intention d’implémenter Analytics sur l’ensemble des appareils à l’aide de la méthode graphique d’appareil, les éléments suivants étaient requis.

>[!WARNING]
>
>Si toutes les conditions préalables ne sont pas remplies, il peut être impossible d’activer Analytics sur l’ensemble des appareils ou le regroupement des données peut donner de mauvais résultats.

* Votre organisation doit utiliser le [graphique privé du service d’identités Adobe Experience Platform](https://business.adobe.com/products/experience-platform/identity-service.html). Consultez également la section [Page d’accueil](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html) dans le guide d’utilisation d’Identity Service.
* Votre mise en œuvre doit utiliser la dernière version du service Experience Cloud ID (ECID). Voir [Page d’accueil](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=fr) dans le guide d’utilisation d’ID Service. Il est probable que le service d’ID soit déjà déployé pour la plupart des implémentations utilisant [Tags](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=fr) dans Adobe Experience Platform.
* Votre implémentation doit appeler la fonction `setCustomerIDs` (ou l’équivalent SDK) chaque fois qu’un individu peut être identifié, par exemple lorsqu’un utilisateur se connecte ou ouvre un e-mail. Cette exigence s’applique à toutes les plateformes, y compris les applications mobiles si elles sont utilisées. Voir [`setCustomerIDs`](https://experienceleague.adobe.com/docs/id-service/using/id-service-api/methods/setcustomerids.html) dans le guide d’utilisation du service d’ID.

## Limites spécifiques au graphique de l’appareil

* Les identifiants Analytics hérités ne sont pas pris en charge. Seuls les visiteurs possédant un Experience Cloud ID sont regroupés.
* Si votre entreprise utilise un graphique privé, l’assemblage des nouveaux appareils peut prendre jusqu’à 24 heures.
* Les graphiques d’appareils tiers ne sont pas pris en charge.
