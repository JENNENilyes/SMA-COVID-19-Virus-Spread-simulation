# SMA-COVID-19-Virus-Spread-simulation
Ce projet consiste à faire un système multi agent pour une simulation de la pandémie actuelle de COVID-19 pour faire face au diffèrent scenarios et faire des prédictions et des recommandations au public  

## Déroulement
	Une population initiale d'agents (personnes de couleur bleue) est placée aléatoirement dans l'espace modèle avec une population initiale d'individus infectés (rouge). Au fur et à mesure que le temps avance, les agents se déplacent aléatoirement dans l'espace modèle en fonction de paramètres spécifiés tels que le nombre d'individus stationnaires et la mobilité. Les individus infectés transmettent le virus aux individus sensibles en s'approchant à une certaine distance les uns des autres. Le fait que l'individu sensible soit infecté est déterminé par une probabilité aléatoire, dont la vraisemblance augmente avec le taux de transmission. 
	Les individus infectés deviendront immunisés (la couleur passe au gris) selon une probabilité aléatoire, dont la probabilité augmente avec l'augmentation du taux de guérison. Le taux de mortalité peut être ajusté. La capacité des hôpitaux à faire face à la proportion d'individus infectés peut également être ajustée. Lorsque la proportion d'individus infectés est supérieure à la capacité des soins de santé, la mortalité augmente d'un ordre de grandeur.


## Paramétrage
init-population
Contrôlez la taille de la population en ajustant le curseur init-population.
init-infected
Contrôle le nombre initial d'infectés à l'aide du curseur init-infected.
Transmission-rate
Current estimates are between 0.50 and 0.70. Set transmission rate by moving the transmission-rate slider.
Stationnary
Le curseur stationnaire permet à l'utilisateur de contrôler le nombre d'individus qui ne se déplacent pas (représentant la distance physique/sociale) dans l'espace du modèle.
Mobilité
Le curseur de mobilité permet à l'utilisateur de définir la distance à laquelle les individus non stationnaires se déplacent dans l'espace du modèle.
Recovery-rate
Set the recovery.rate slider low for longer recovery time and high for quick recovery. Suggested recovery rate for the current virus is 0.15.
Quarantine-effort
En ajustant le curseur quarantine.effort, les utilisateurs peuvent contrôler la capacité des individus infectés à infecter les personnes sensibles.
Healthcare-capacity
Le curseur healthcare.capacity modifie la proportion de personnes infectées que les hôpitaux peuvent prendre en charge.
Infected-mortality
Le curseur infected.mortality modifie le taux de mortalité de base pour les personnes infectées. Les estimations du taux de mortalité vont de 1 à 10 %, avec une moyenne d'environ 3,6 si l'on ne tient pas compte de la capacité des soins de santé.
![image](https://user-images.githubusercontent.com/64171895/155888448-18f9b51e-00ab-4aea-a84a-02e9f1c38e34.png)

 
## Agents
•	Les individus : ce déplace d’une façon aléatoire dans l’environnement et ayant une vue locale sur ce dernier
		Individus sains : couleur bleu
		Individus infectés : couleur rouge, ce type peut infecter les individus 			sains qui se présentent près de lui
		Individus immunes : couleur gris

•	Hôpital : son rôle est le suivie sanitaire
	- Inspecter les individus
-	Traiter les individus infectés (soit il est guérit ou il va mourir)
