---
title: Test caché
description: Il s’agit d’un test masqué
hide: true
hidefromtoc: true
landing-page-breadcrumb-title: Test AEM 6.5
landing-page-name: experience-manager-65
feature: Annotations
hold: true
exl-id: e6e5ba1c-98a5-4d7d-9913-426df31bc7a3
source-git-commit: f38dd5701562d9e51256c50f766c7b03f253f279
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 7%

---

# Test caché

2 février 2026 - `hold: true` est activé. Oh, c&#39;est comme ça !
3 février 2026 - Matt

Il s’agit d’un test masqué. J’ajoute ce `[` pour m’assurer qu’il fonctionne correctement dans le rendu v2.

## Ouvrir dans un nouvel onglet {#section_92882928}

`[See What's new](auditor.md) {target="_blank"}`

[Ouvrir dans le même onglet](auditor.md)

[Nouvel onglet avec espace et guillemets](auditor.md) {target="_blank"}

[Nouvel onglet avec ancre](auditor.md){target=« _blank}

[Nouvel onglet sans espace avec guillemets](auditor.md){target="_blank"}

[Nouvel onglet sans guillemets](auditor.md) {target=_blank}

[Nouvel onglet sans espace sans guillemets](auditor.md){target=_blank}

[Nouvel onglet avec lien profond](commerce-channels.md#channel-manager-extension){target="_blank"}

[Ancrer le nouvel onglet avec le lien profond](https://experienceleague.adobe.com/en/docs/analytics/analyze/home#key-analytics-resources){target="_blank"}

[Nouvel onglet avec lien externe](https://www.adobe.com){target="_blank"}

[Nouveau lien racine de l’onglet](/help/guide-1/auditor.md){target="_blank"}


<table>
  <tr>
    <th>Avec des guillemets</a></th>
    <th>Sans guillemets</th>
  </tr>
  <tr>
    <td><a href="https://www.adobe.com" target="_blank">Nouvel onglet Adobe</a></td>
    <td><a href="https://www.adobe.com" target="_blank">Nouvel onglet Adobe</td>
  </tr>
  <tr>
    <td><a href="https://www.adobe.com">Adobe : aucun nouvel onglet</a></td>
    <td><a href="https://www.adobe.com">Adobe : aucun nouvel onglet</td>
  </tr>
</table>

## Test de commentaire

18 Novembre 2025

<!-- ## Comment with basic text

This is a new line.

Second new line. -->


Commentaire ci-dessous. Si c&#39;est la dernière chose que vous voyez dans cet article, c&#39;est en raison de la syntaxe du commentaire.

1. Cliquez sur **[!UICONTROL Créer]**.

<!-- ## Create an exclusion using Advanced Search

You can also create exclusions using [!UICONTROL Advanced Search] on the [Catalog Search](/help/main/c-recommendations/c-products/catalog-search.md#save-as) page ( [!UICONTROL Recommendations] > [!UICONTROL Catalog Search] > [!UICONTROL Advanced Search]). 

![Save as dialog](/help/main/c-recommendations/c-products/assets/save-as.png)

After creating a search using "id > contains," for example, you can then click [!UICONTROL Save As] > [!UICONTROL Exclusion].

>[!IMPORTANT]
>
>The [!UICONTROL Advanced Search] functionality is case-insensitive; however, products returned at the time of delivery are based on case-sensitive search. This mismatch might lead to confusion. Ensure that you consider case-sensitivity when you create exclusions based on results using the Advanced Search functionality. For example, if you perform a search for "Holiday," that initial search lists results containing "Holiday" and "holiday." If you then create an exclusion with the intent to exclude products containing "holiday," only products containing "holiday" are excluded. Products containing "Holiday" are not excluded. -->

Cette ligne se trouve après le commentaire.

## Test vidéo

### Vidéo simple sans transcription : doit afficher la transcription, car metadata.md est distribué.

>[!VIDEO](https://video.tv.adobe.com/v/332116?hidetitle=true)

### Avec le relevé de notes défini sur true

>[!VIDEO](https://video.tv.adobe.com/v/332116?hidetitle=true){transcript=true}

### Lorsque la transcription est définie sur false, la transcription vidéo ne doit pas s’afficher

>[!VIDEO](https://video.tv.adobe.com/v/332116?hidetitle=true){transcript=false}

## Liens relatifs

* [Vue d’ensemble](overview.md)
* [Rechercher et promouvoir](search-promote.md)
* [Social](social.md)

## Lien profond explicite

[présentation supplémentaire (racine)](/help/guide-1/overview.md#additional-products)

[présentation supplémentaire](overview.md#additional-products)

## Test de texte avec pointage {#this-is-a-heading-anchor}

Pas de texte de pointage

```
![alt text](assets/maui-flip.jpg)
```

![texte alternatif](assets/maui-flip.jpg)


Oui, survoler le texte

```
![alt text](assets/maui-flip.jpg "Hover text")
```

![texte secondaire](assets/maui-flip.jpg "texte de survol")

## Diapositive

Syntaxe :

```
>[!SLIDE](analyze-project)
https://experienceleague-stage.adobe.com/en/slides/analyze-project
```

Rendu :

<!--
>[!SLIDE](analyze-project)
-->

Bob : Supprimez le commentaire de diapositive une fois que vous avez testé le verrou de rubrique.
