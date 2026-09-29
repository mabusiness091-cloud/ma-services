# Suppression des comptes M&A Services

La demande est créée depuis **Client → Mon compte → Paramètres du compte**.
Elle apparaît dans **Administration M&A → Suppressions de comptes**. Apple
autorise un traitement manuel si l'utilisateur connaît le délai et reçoit une
confirmation après la suppression. Le site annonce un traitement sous 30 jours.

## Traitement d'une demande

1. Ouvrir la demande dans l'administration, vérifier que l'identifiant et le
   contact correspondent au titulaire authentifié. Les comptes utilisent la
   même identité Supabase dans les espaces Client, Prestataire, Marketplace,
   Transport et Éducation.
2. Rechercher les données liées à cet identifiant dans tous les modules :
   profil, demandes clients et transport, prestataires et pièces de vérification,
   établissements et préinscriptions, produits et photos, notifications et
   commandes. Vérifier les contrats et paiements avant toute suppression.
3. Supprimer les fichiers du titulaire dans Supabase Storage, puis effacer ou
   anonymiser ses données personnelles et contenus. Conserver seulement les
   éléments qu'une obligation légale impose de garder, en documentant la raison.
   Une commande partagée avec un autre utilisateur demande une revue humaine :
   ne pas détruire les données de cet autre utilisateur.
4. Supprimer **ensuite** l'utilisateur depuis Supabase Authentication → Users.
   La ligne `account_deletion_requests` disparaît avec l'utilisateur.
5. Envoyer une confirmation au contact qui figurait dans la demande après
   vérification de l'effacement. Supprimer toute copie temporaire du contact.

Ne jamais publier la clé `service_role` dans le navigateur, dans le dépôt Git
ou dans l'application iOS. La suppression du compte est une opération
irréversible : ne jamais la lancer sur un utilisateur réel pour tester l'UI.
