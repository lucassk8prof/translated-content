---
title: NodeIterator.nextNode()
slug: Web/API/NodeIterator/nextNode
tags:
  - API
  - Arborescence
  - DOM
  - Itérateur
  - Méthodes
  - Noeuds
translation_of: Web/API/NodeIterator/nextNode
---
{{APIRef("DOM")}}

La méthode **`NodeIterator.nextNode()`** renvoie le noeud suivant dans l'ensemble représenté par le {{domxref("NodeIterator")}} et avance la position de l'itérateur dans cet ensemble.  Le premier appel de `nextNode()` en renvoie le premier noeud.

Cette méthode retourne `null` quand il n'y a plus de nœuds dans l'ensemble.

Dans les navigateurs anciens, comme spécifié dans les anciennes version des spécifications, la méthode pouvait déclencher une {{domxref("DOMException")}}   `INVALID_STATE_ERR` si elle était appelée après la méthode {{domxref("NodeIterator.detach()")}}. Les navigateurs récents ne lancent rien.

## Syntaxe

    node = nodeIterator.nextNode();

## Exemple

```js
var nodeIterator = document.createNodeIterator(
    document.body,
    NodeFilter.SHOW_ELEMENT,
    { acceptNode: function(node) { return NodeFilter.FILTER_ACCEPT; } },
    false // this optional argument is not used any more
);
currentNode = nodeIterator.nextNode(); // renvoie le noeud suivant.
```

## Spécifications

| Spécification                                                                                                                                        | Statut                                       | Commentaire                                                                                       |
| ---------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| {{SpecName('DOM WHATWG', '#dom-nodeiterator-nextnode', 'NodeIterator.nextNode')}}                                         | {{Spec2('DOM WHATWG')}}             | Comme `detach()` est maintenant une méthode non opérante, cette méthode ne peut plus rien lancer. |
| {{SpecName('DOM2 Traversal_Range', 'traversal.html#Traversal-NodeIterator-nextNode', 'NodeIterator.nextNode')}} | {{Spec2('DOM2 Traversal_Range')}} | Définition initiale.                                                                              |

## Compatibilité des navigateurs

{{Compat("api.NodeIterator.nextNode")}}

## Voir aussi

L'interface à laquelle elle appartient : {{domxref("NodeIterator")}}.
