# Authentification twitter

## Sujet
```
Trouver un mot de passe twitter
```

## Résolution
- ouvrire le fichier avec **WireShark**
- ouvrire l'onglet **Analyser**
- suivre le **flux TCP**
- voyons après le mot **Authorization** qui correspont à une requête HTTP contient les identifiants permettant l'authentification d'un utilisateur auprès d'un serveu
- en argument à cette requète, on a :
```
Authorization: <type> <credentials>
```
- le **credentials** contient le nomd'utilisateur et le mot de passe  combinés par avec deux-point, et encodée ensuite en **base64**
- il faut décoder ce dernier pour avec l'utilisateur et le mot de passe