# Allocation dynamique des ressources dans le cloud

Nous considérons le problème d’allocation des VMs dans un serveur physique d’un cloud en tenant compte de la charge, et du nombre de VM en fonctionnement. On contrôle le système en décidant d’allouer ou désallouer des VMs.


On a K le nombre maximal de VMs donc le nombre de serveurs actifs $n \in \{0,1,\ldots,K\}$. 

On a B la capacité maximale du système donc le nombre de clients dans le système $m \in \{0,1,\ldots,B\}$

Pour la modélisation du problème on a codé les états $s=(m,n)$ en une seule dimension telle que $s = m+n(B+1)$. On a donc $s \in \{0,1,\ldots,(B+1)\times(K+1)-1\}$.


La matrice de transition $P$ est une donc une matrice de dimensions $nombre\space d'états\times nombre\space d'actions \times nombre\space d'états$ : la première dimension correspond à l'état actuel, la deuxième à l'action et la troisième à l'état suivant.

On a donc $P_{s,\alpha,s'}$ la probabilité de passer de l'état $s$ à l'état $s'$ en effectuant l'action $\alpha$.

On cherche à implémenter plusieurs méthodes d'apprentissage par renforcement pour ce problème : Q-Learning et SARSA.
