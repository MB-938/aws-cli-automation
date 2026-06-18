# AWS CLI Automation

> **FR** — Automatisation des opérations AWS depuis le terminal : création d'instances EC2, gestion des Security Groups, paires de clés, utilisateurs IAM, groupes et politiques — sans toucher la console AWS.
>
> **EN** — Automating AWS operations from the terminal: creating EC2 instances, managing Security Groups, key pairs, IAM users, groups, and policies — without touching the AWS console.

---

## Stack

![AWS CLI](https://img.shields.io/badge/AWS-CLI-orange?logo=amazonaws)
![EC2](https://img.shields.io/badge/AWS-EC2-orange?logo=amazonaws)
![IAM](https://img.shields.io/badge/AWS-IAM-orange?logo=amazonaws)

---

## FR — Ce qui a été réalisé

### EC2 via CLI
- Installation et configuration du CLI (`aws configure`, profils, variables d'environnement)
- Création d'un Security Group et d'une paire de clés RSA
- Lancement d'une instance EC2 (Amazon Linux, t3.micro) entièrement en ligne de commande
- Connexion SSH à l'instance
- Utilisation de `--filters` et `--query` (JMESPath) pour filtrer les résultats côté serveur et côté client

### IAM via CLI
- Création de groupes, utilisateurs et ajout d'un utilisateur à un groupe
- Attachement de politiques managées AWS (`AmazonEC2FullAccess`)
- Création de politiques personnalisées depuis un fichier JSON local
- Création de profils de connexion console avec mot de passe temporaire
- Génération de clés d'accès programmatiques
- Basculement entre contextes IAM via variables d'environnement

## EN — What was done

### EC2 via CLI
- Installation and configuration of the CLI (`aws configure`, profiles, environment variables)
- Created a Security Group and an RSA key pair
- Launched an EC2 instance (Amazon Linux, t3.micro) entirely from the command line
- SSH connection to the instance
- Used `--filters` and `--query` (JMESPath) to filter results server-side and client-side

### IAM via CLI
- Created groups, users, and added a user to a group
- Attached AWS managed policies (`AmazonEC2FullAccess`)
- Created custom policies from a local JSON file
- Created console login profiles with a temporary password
- Generated programmatic access keys
- Switched between IAM contexts via environment variables

---

## FR — Concepts clés

| Concept | Description |
|---|---|
| `--filters` | Filtre les ressources **côté serveur** (AWS ne renvoie que ce qui correspond) |
| `--query` | Filtre les champs **côté client** via la syntaxe JMESPath |
| ARN | Identifiant unique d'une ressource AWS (`arn:aws:service::account-id:resource`) |
| `/32` CIDR | Restriction d'accès à une seule adresse IP |
| Env vars IAM | Surchargent `~/.aws/credentials` pour la session shell en cours uniquement |

## EN — Key Concepts

| Concept | Description |
|---|---|
| `--filters` | Filters resources **server-side** (AWS only returns matching resources) |
| `--query` | Filters fields **client-side** using JMESPath syntax |
| ARN | Unique identifier for an AWS resource (`arn:aws:service::account-id:resource`) |
| `/32` CIDR | Restricts access to a single IP address |
| IAM env vars | Override `~/.aws/credentials` for the current shell session only |

---

## Files

| File | Description |
|---|---|
| `README.md` | Step-by-step guide with all commands and explanations |
| `aws-cli-commands.md` | Quick reference command cheatsheet |
