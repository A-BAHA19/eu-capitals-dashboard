# Réflexions — TD1

## 1. Mon choix entre météo et émissions de CO₂
Pour choisir une destination de vacances, j’accorderais autant d’importance à la météo qu’aux émissions de CO₂ du trajet, soit une pondération de 50 % pour chaque critère. Je chercherais donc un compromis entre des conditions météorologiques agréables et un impact environnemental limité.

## 2. Fiabilité de l’acquisition des données

Faire 26 requêtes séparées multiplie les risques de rencontrer une erreur de connexion, un délai dépassé ou une limitation du service météo. Une seule requête regroupant les 26 capitales réduit ces risques et permet aussi de récupérer les données plus rapidement.

## 3. Vérification du facteur d’émission de CO₂

Avant de publier ce tableau de bord pour de vrais voyageurs, je vérifierais le facteur de 0,15 kg CO₂e par kilomètre et par passager dans une source officielle récente, comme les données DEFRA. Je vérifierais les hypothèses utilisées, notamment le type de vol et les effets climatiques inclus. J’indiquerais la source, son année et les limites de cette estimation, puis je prévoirais sa mise à jour.

## 4. Mesure réelle et score relatif

L’ajout d’une capitale particulièrement froide et pluvieuse ne changerait pas les mesures météorologiques des autres villes. Cependant, leurs scores normalisés pourraient changer, car ils sont calculés à partir des valeurs minimales et maximales de la liste. Une mesure décrit une grandeur observée, tandis qu’un KPI est un indicateur construit selon une méthode et un ensemble de comparaison.

## 5. Ma prédiction avant l’exécution

Je prédis que Rome arrivera en tête, car je m’attends à une météo agréable et à une distance depuis Paris plus faible que celle de certaines destinations plus éloignées. Elle pourrait donc offrir un bon compromis avec une pondération de 50 % pour la météo et de 50 % pour les émissions de CO₂.

## 6. Comparaison entre ma prédiction et le résultat

J’avais prédit que Rome arriverait première, mais le classement obtenu place Madrid en tête, suivie de Lisbonne puis de Rome. Ma prédiction n’est donc pas confirmée, même si Rome figure parmi les trois premières destinations. Avec les données météo récupérées et la pondération 50 % météo / 50 % CO₂, Madrid obtient le meilleur score global.

## 7. Surveillance des mises à jour

La date de dernière mise à jour affichée sur la page permet de repérer un arrêt de la mise à jour des données. Si elle reste ancienne alors qu’un calcul est prévu chaque lundi, cela peut signaler un problème. J’ajouterais un avertissement visible lorsque les données ont plus de huit jours, ainsi qu’une alerte au responsable en cas d’échec du programme.

## 8. Changement de ville de départ

J’ai modifié scripts/fetch_and_score.py pour calculer les distances et les émissions de CO₂ depuis Le Mans. J’ai également supprimé l’exclusion de Paris : Le Mans n’étant pas dans la liste, les 27 capitales sont désormais des destinations possibles. J’ai adapté docs/index.html pour afficher la nouvelle ville de départ et le nombre de destinations.

Après une nouvelle exécution réussie, Madrid reste première, suivie de Lisbonne puis de Paris. La meilleure destination dépend donc du point de départ, des prévisions météo et des critères choisis : ce n’est pas une propriété absolue d’une ville.
