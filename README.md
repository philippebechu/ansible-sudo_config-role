Role Name
=========

Role de gestion des fichiers sudoers.

Les fichiers sudoers présents sont déployés un par un. La cohérence est testée via la commande visudo -cs.
Si la commande échoue, le dernier fichier déployé est supprimé.

Requirements
------------


Role Variables
--------------

sudo_files : liste des fichiers à déployer.
Doivent être présents dans le dossier files/sudoers/ (TODO : variabilisation)

Dependencies
------------


Example Playbook
----------------

  vars:
    sudo_files:
      - default
      - externes

  roles:
    - role: sudo_config

License
-------


Author Information
------------------

An optional section for the role authors to include contact information, or a
website (HTML is not allowed).
