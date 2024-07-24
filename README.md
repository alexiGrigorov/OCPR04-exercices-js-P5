# OCPR4-exercices-js-P5

Testez vos compétences : les langages du Web

Pour commencer le projet, lancez la commande `npm install` qui installera les dépendances du projet.

Vous pourrez ainsi réaliser les différents exercices.

Pour vérifier que votre exercice est correctement réalisé vous n'avez qu'à lancer la commande `npm start` puis la commande `npm run test`.
Vous verrez alors s'afficher l'application `Cypress`.
Sélectionnez `E2E Testing` puis sélectionnez le navigateur dans lequel vous voulez lancer vos tests.

Si votre code est correct alors les tests seront décrits en vert.

Bon entraînement !

## Resultats des tests

### Exercice 1

![](./Resultats/Exercice_1_résultats.JPG)

### Exercice 2

![](./Resultats/Exercice_2_résultats.JPG)

### Exercice 3

![](./Resultats/Exercice_3_résultats.JPG)

### Exercice 4

Le test initial était erroné:

```
it('Should have a shadow on header and footer box shadow', () => {
cy.get('header').should('exist').and('have.css', 'box-shadow').and('not.contain.value', 'none')
cy.get('footer').should('exist').and('have.css', 'box-shadow').and('not.contain.value', 'none')
})
```

Le test a été corrigé et remplacé par:

```
it("Should have a shadow on header and footer box shadow", () => {
    cy.get("header")
      .should("exist")
      .and("have.css", "box-shadow")
      .should("not.equal", "none");
    cy.get("footer")
      .should("exist")
      .and("have.css", "box-shadow")
      .should("not.equal", "none");
  });
```

![](./Resultats/Exercice_4_résultats.JPG)

### Exercice 5

![](./Resultats/Exercice_5_résultats.JPG)

### Exercice 6

Le test initial était erroné:

```
it('Should have blue li', () => {
      cy.get('li').each($li => {
          expect($li).to.have.css('color', 'rgb(0, 0, 255)');
          expect($li).to.have.css('padding-left', '10px');
          expect($li).to.have.css('margin-bottom', '15px');
      })
  })
```

Le test a été corrigé et remplacé par:

```
it("Should have blue li", () => {
    cy.get("li").each(($li) => {
      expect($li).to.have.css("color", "rgb(0, 123, 255)");
      expect($li).to.have.css("padding-left", "10px");
      expect($li).to.have.css("margin-bottom", "15px");
    });
  });
```

![](./Resultats/Exercice_6_résultats.JPG)

### Exercice 7

![](./Resultats/Exercice_7_résultats.JPG)

### Exercice 8

![](./Resultats/Exercice_8_résultats.JPG)

### Exercice 9

![](./Resultats/Exercice_9_résultats.JPG)

### Exercice 10

![](./Resultats/Exercice_10_résultats.JPG)
