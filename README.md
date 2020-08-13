# Mtn Mobile Money Api In Production (PHP)

    Il s'agit d'une Class php qui a été conçue pour aider les développeurs à intégrer facilement ** momo api ** dans leur système.

## Prerequisites ##

    Avant de commencer à utiliser cette Class, nous supposons que vous avez une bonne connaissance en php.
    Et avoir installé tous les logiciels requis pour permettre d'exécuter les exemples fournis ici.
    Vous devez également avoir un compte sur le portail des développeurs Momo 
[https://momodeveloper.mtn.com/](https://momodeveloper.mtn.com/ "Visit page")

    Deplus vous devez avoir  créer

    - **ApiUser** 
    - **ApiKey** 
[https://momo.mtncameroon.net/partner/](https://momo.mtncameroon.net/partner/ "Visit page")

## Installation ##

    Ouvrez le fichier momoapi.php et remplicez les informations

***momoapi.php***

    <?php
        
        $this->_disPrimKey = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX";
        $this->_disSecdKey = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX";
        $this->_disApiUser = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX";
        $this->_disApiKey =  "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX";

        $this->_colPrimKey = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX";
        $this->_colSecdKey = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX";
        $this->_colApiUser = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX";
        $this->_colApiKey =  "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX";
    
        $this->colPayerMessage = "payerMessage";
        $this->colPayeeNote = "payeeNote";

        $this->disPayerMessage = "payerMessage";
        $this->disPayeeNote =  "payeeNote";

Ensuite inclure le fichier momoapi.php dans votre projet

    <?php 
         require_once 'momoapi.php';

            $momo = new  MOMOAPI();

## Utilisation ##

***collections.php***

    <?php 
            // montant  237+numero	uniquecode
             $momo->colRequestToPay("montant","23767xxxxxx","uniquecode");

***collections_status.php***

    <?php 
            // Reference-Id
             $momo->colStatus("1c2d671d-d00d-43a9-92ea-25ea8aab9cb1");

***disbursements.php***

    <?php 
            // montant  237+numero	uniquecode
             $momo->disTransfer("montant","23767xxxxxx","uniquecode");

***disbursements_status.php***

    <?php 
            // Reference-Id
             $momo->disTransferStatus("1c2d671d-d00d-43a9-92ea-25ea8aab9cb1");