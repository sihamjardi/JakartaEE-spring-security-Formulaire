# JakartaEE-spring-security-Formulaire

## Objectif

Ce TP vise à comprendre et personnaliser le mécanisme d’authentification de Spring Security.
L’objectif est de remplacer la page de connexion par défaut de Spring par un formulaire HTML personnalisé, tout en gérant :

les erreurs de connexion,
les redirections après authentification,
la déconnexion,
et la différenciation des accès selon les rôles.
Ce TP fait suite au TP (authentification en mémoire) et introduit la notion de flux d’authentification contrôlé par l’application.

---

## Introduction conceptuelle
Par défaut, Spring Security fournit une interface de connexion prête à l’emploi, mais très basique.
Dans un contexte professionnel, cette interface doit :

s’intégrer à l’identité visuelle du site,
offrir une meilleure ergonomie,
afficher des messages d’erreur clairs,
et gérer des redirections adaptées au rôle de l’utilisateur.
Spring Security permet cela sans redéfinir tout le mécanisme d’authentification : il suffit de brancher un formulaire HTML sur les endpoints contrôlés par le framework (/login, /authenticate, /logout, etc.).

---

## Compétences à acquérir
À la fin de ce TP, l’étudiant doit être capable de :

•Décrire le flux complet d’authentification dans Spring Security.

•Configurer un formulaire de login personnalisé.

•Gérer les redirections après succès ou échec.

•Comprendre le rôle de chaque composant (HttpSecurity, UserDetailsService, SecurityFilterChain).

•Implémenter une page de logout propre.

---

## Structure du projet

<img width="228" height="441" alt="image" src="https://github.com/user-attachments/assets/db6afe03-9339-42bc-9a0b-a405c7f15c5b" />


---

## Étape – Test complet du flux

**L’accès sans login**

***http://localhost:8080/login***

<img width="919" height="479" alt="Capture d&#39;écran 2025-11-24 002528" src="https://github.com/user-attachments/assets/515b0080-26f6-48ae-8a90-dde5ac0d49d8" />

**Admin**

<img width="924" height="496" alt="Capture d&#39;écran 2025-11-24 002706" src="https://github.com/user-attachments/assets/595dfb0d-d8d0-4839-abcd-b4f8cbd64a6e" />
<img width="928" height="494" alt="Capture d&#39;écran 2025-11-24 002715" src="https://github.com/user-attachments/assets/f8415921-41f5-4db5-ab42-7d1494b8db9f" />
<img width="923" height="500" alt="Capture d&#39;écran 2025-11-24 002725" src="https://github.com/user-attachments/assets/9bb61565-5086-46df-b1e8-5b9c8a906e1b" />
<img width="923" height="503" alt="Capture d&#39;écran 2025-11-24 002738" src="https://github.com/user-attachments/assets/9d353454-3f56-4f15-a75e-c419756e869e" />




**User**

<img width="923" height="493" alt="Capture d&#39;écran 2025-11-24 002620" src="https://github.com/user-attachments/assets/adc8d734-dcc0-4aed-897b-af8322849776" />
<img width="925" height="475" alt="Capture d&#39;écran 2025-11-24 002628" src="https://github.com/user-attachments/assets/bfa4517a-f72c-491e-bb78-10caeeb0196a" />
<img width="923" height="488" alt="Capture d&#39;écran 2025-11-24 002638" src="https://github.com/user-attachments/assets/8874c11a-5ced-4325-a123-eb3841449d3d" />
<img width="922" height="488" alt="Capture d&#39;écran 2025-11-24 002648" src="https://github.com/user-attachments/assets/731d2875-71d3-48a1-a2c8-e3f572090a59" />










