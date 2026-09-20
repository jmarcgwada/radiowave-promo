# RadioWave — page de presentation

La vitrine de l'application **RadioWave** : ce qu'elle fait, a quoi elle
ressemble, ou la telecharger.

- En ligne : <https://jmarcgwada.github.io/radiowave-promo/>
- Contenu : [index.html](index.html) — une page autonome d'environ 215 ko,
  captures d'ecran comprises — et [og.png](og.png), l'image d'apercu du partage.

## Une seule page, et pourquoi

Pas de generateur de site, pas d'etape de construction, aucune dependance a
installer : on modifie `index.html`, on envoie sur `main`, GitHub Pages
republie. Pour une page de presentation qui change quelques fois par an, c'est
le meilleur rapport entre le resultat et ce qu'il faut entretenir.

Le revers est assume : le fichier est gros parce que les captures d'ecran y sont
integrees directement. C'est ce qui lui permet de s'afficher d'un seul coup,
sans attendre une douzaine d'images.

Seules ressources chargees de l'exterieur : les polices Google
(Bricolage Grotesque, Manrope, Space Mono).

## Ce que la page contient

| Section | Propos |
| --- | --- |
| Pensee pour ecouter la radio comme en 2026 | L'idee de depart |
| Un coup d'oeil a RadioWave | Les captures d'ecran de l'application |
| La ou on veut emmener la radio | Ce qui est prevu |
| Une seule appli, tous tes ecrans | Telephone, tablette, ordinateur |
| Le monde passe a la radio | La couverture mondiale des stations |

Elle renvoie vers le **mini-lecteur web**
(<https://jmarcgwada.github.io/radiowave-listen/>), vers un **formulaire Google**
pour les retours, et propose le partage WhatsApp et Facebook.

## L'apercu du partage

`og.png` est l'image qui apparait quand on colle le lien dans un message ou sur
un reseau social. Les balises `og:` et `twitter:` de l'en-tete pointent vers des
adresses **absolues** : un chemin relatif ne fonctionnerait pas, puisque c'est
Facebook ou WhatsApp qui va chercher l'image, pas le navigateur du visiteur.

Si vous remplacez `og.png`, forcez une relecture avec le
[debogueur de partage de Facebook](https://developers.facebook.com/tools/debug/) —
les apercus restent en cache longtemps.

## Modifier

1. Editer `index.html`.
2. Envoyer sur `main`.
3. GitHub Pages republie dans la minute.

Les captures d'ecran sont encodees dans le fichier. Pour en remplacer une,
reperez le bloc `data:image/...` correspondant : c'est la partie la plus lourde
du fichier, et la seule vraiment penible a modifier a la main.

## Projets lies

- **RadioWave** — l'application mobile.
- **radiowave-listen** — le mini-lecteur web vers lequel cette page renvoie.
- **radiowave-legal** — la politique de confidentialite exigee par les magasins.
