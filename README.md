# Classification_risk_analysis

# ΕΙΣΑΓΩΓΗ


Είναι σύνηθες πλέον να χρησιμοποιούμε τεχνικές τεχνητής νοημοσύνης για να διευκολύνουμε την καθημερινότητα μας ή και να βρίσκουμε λύσεις σε προβλήματα όπου ένα ανθρώπινο μυαλό θα ήταν αρκετά χρονοβόρο έως και αδύνατον να δώσει. Η ανάγκη για την δημιουργία  μοντέλων  τα οποία λειτουργούν ως ταξινομητές προήλθε από το γεγονός ότι έχουν πληθώρα εφαρμογών. Π.χ:

    α)Διαχωρισμός των emails με βάση την επικεφαλίδα τους ή το περιεχόμενο.
    β)Πρόβλεψή καρκινικών κυττάρων χαρακτηρίζοντας τα ως καλοήθη η κακοήθη.
    
Αυτό που καλούμαστε εμείς να κάνουμε είναι μέσα από τα δεδομένα που μας δίνονται από αρχείο excel να καταφέρουμε να φτιάξουμε ένα μοντέλο το οποίο: 



    1) θα μπορεί να βρίσκει με ποσοστό επιτυχίας τουλάχιστον 62 % τις εταιρείες που θα πτωχεύσουν.

    2) θα μπορεί να βρίσκει με ποσοστό επιτυχίας τουλάχιστον 70 % τις εταιρείες που δεν θα πτωχεύσουν.

Οι παρατηρήσεις για την κάθε εταιρία είναι οι παρακάτω:

• Οι δείκτες απόδοσηςτων εταιρειών (στήλες Α έως και Η) 
      
    1) 365* ( Β.Υ / Κοστ.Πωλ )
    2) Λειτ.Αποτ/Συν.Ενεργ. (ROA)
    3) ΧΡΗΜ.ΔΑΠΑΝΕΣ / ΠΩΛΗΣΕΙΣ
    4)  ΠΡΑΓΜΑΤΙΚΗ ΡΕΥΣΤΟΤΗΤΑ :  (ΚΕ-ΑΠΟΘΕΜΑΤΑ) / Β.Υ
    5) (ΑΠΑΙΤ.*365) / ΠΩΛ.
    6) Συν.Υποχρ/Συν.Ενεργ
    7) Διάρκεια Παραμονής Αποθεμάτων
    8) Λογαριθμος Προσωπικού
       
• Τρεις δυϊκοί δείκτες δραστηριοτήτων (στήλες I, J, K) 
      
    9) ΕΝΔΕΙΞΗ ΕΞΑΓΩΓΩΝ 
    10) ΕΝΔΕΙΞΗ ΕΙΣΑΓΩΓΩΝ
    11) ΕΝΔΕΙΞΗ ΑΝΤΙΠΡΟΣΩΠΕΙΩΝ

12) Η κατάσταση της εταιρείας (1 όλα καλά, 2 έχει κηρύξει χρεωκοπία) 

13) Το έτος στο οποίο αφορούν τα ως άνω μεγέθη. 

Αποφάσισα να υλοποιήσω 7 μοντέλα ταξινομητών τα οποία είναι τα παρακάτω:

    1. Λογιστική Παλινδρόμηση (Logistic Regression) 
    2. Δέντρα Απόφασης(Decision Trees) 
    3. Κ –Πλησιέστεροι Γείτονες (k-­‐Nearest Neighbors 
    4. Γραμμική Διακριτική Ανάλυση (Linear Discriminant Analysis) 
    5. Ταξινομητής Naïve Bayes 
    6. Μηχανές ΔιανυσμάτωνΥποστήριξης (Support Vector Machines) 
    7. Τεχνητά Νευρωνικά Δίκτυα(Artificial Neural Networks) 
    
Για να μετρήσουμε την απόδοση του κάθε μοντέλου θα χρησιμοποιούμε τις παρακάτω συναρτήσεις.

    1. Precision: πόσα από τα παραδείγματα που το μοντέλο υπολόγισε ότι ανήκαν στην ομάδα Χ, ανήκαν όντως στην ομάδα Χ. 
    2. Recall: από το σύνολο των παραδειγμάτων που ανήκαν στην ομάδα Χ, πόσα ανέκτησε το μοντέλο. 
    3. F1 score: αρμονικός μέσος των precision και recall. Βοηθά στο να έχουμε μια γενική ιδέα της απόδοσης του μοντέλου.
    
Στο παρων project ερχομαστε αντιμετοποι με ενα  "unbalanced dataset" και παρουσιαζουμε 3 διαφορετικες τεχνικες αντιμετοπισης.

     1) Under Sampling
     2) Oversampling
     3) Smote
     
     
## Installation

### Environment 

I use [Anaconda](https://www.anaconda.com/products/individual) because it comes with many Python
packages already installed and it is easy to work with. After installing Anaconda,
you should create a [conda environment](http://conda.pydata.org/docs/using/envs.html)
so you do not destroy your main installation in case you make a mistake somewhere:

       conda create --name classification python=3.7

Now you can switch to the new environment by running the following:

      conda activate classification


### Required Packages

The Python packages that this project requires are listed in requirements.txt

To install the required Python packages and dependencies you first have to activate the conda-environment as described above, and then you run the following command in a terminal:

      pip install -r requirements.txt
      

