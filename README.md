# Σύστημα Κρατήσεων Εστιατορίου (Capstone Project)

## Ιστορία Εφαρμογής

Έχετε προσληφθεί ως Full Stack Developer στην Periodic Tables, μια startup που αναπτύσσει ένα σύστημα κρατήσεων για εστιατόρια υψηλής γαστρονομίας. Η εφαρμογή χρησιμοποιείται μόνο από το προσωπικό του εστιατορίου όταν οι πελάτες καλούν για να κάνουν κράτηση. Οι πελάτες δεν έχουν άμεση πρόσβαση στο σύστημα μέσω διαδικτύου.

Δημιουργία & Λίστα Κρατήσεων
Οι κρατήσεις δημιουργούνται μόνο:

σε ημέρες λειτουργίας

κατά τις ώρες λειτουργίας (τουλάχιστον 60 λεπτά πριν το κλείσιμο)

Καθιέρωση Κράτησης
Όταν φτάνει ο πελάτης, επιλέγεται τραπέζι για να καθίσει.

-Ολοκλήρωση Τραπεζιού
Όταν οι πελάτες αποχωρούν, το τραπέζι γίνεται ξανά διαθέσιμο.

-Κατάσταση Κράτησης
Οι καταστάσεις είναι: booked, seated, finished

Οι finished κρατήσεις δεν εμφανίζονται στο ταμπλό.

-Αναζήτηση Κράτησης
Αναζήτηση με αριθμό τηλεφώνου (μερικός ή πλήρης αριθμός).

-Επεξεργασία Κράτησης
Δυνατότητα επεξεργασίας ή ακύρωσης υπάρχουσας κράτησης.

Δεδομένα API
Υπάρχουν δύο σύνολα δεδομένων: reservations και tables.


## Ρύθμιση Βάσης Δεδομένων

1. Δημιουργήστε 4 βάσεις ElephantSQL: development, test, preview, production.
2. Συνδέστε τις βάσεις στο DBeaver.

## Knex

Εκτελέστε τις εντολές `npx knex` μέσα στον φάκελο `back-end` όπου βρίσκεται το `knexfile.js`.
Εκτέλεση Δοκιμών
```bash

Copy
Edit
npm run test:X            # Τρέχει όλα τα tests για το user story X
npm run test:X:backend    # Τρέχει μόνο τα backend tests για το user story X
npm run test:X:frontend   # Τρέχει μόνο τα frontend tests για το user story X
Παραδείγματα              
bash
Copy
Edit
npm run test:1
npm run test:3:backend
npm run test:3:frontend
User Stories

Δείγματα:
```bash
json
Copy
Edit
# Κράτηση
{
  "first_name": "Rick",
  "last_name": "Sanchez",
  "mobile_number": "202-555-0164",
  "reservation_date": "2020-12-31",
  "reservation_time": "20:00:00",
  "people": 6
}

# Τραπέζι
{
  "table_name": "Bar #1",
  "capacity": 1
}


## Οδηγίες Εγκατάστασης

# Βήμα 1: Κλωνοποίηση αποθετηρίου
git clone <repository-url>
cd restaurant-reservation

# Βήμα 2: Δημιουργία αρχείων περιβάλλοντος
cp ./back-end/.env.sample ./back-end/.env
# ➤ Ενημερώστε το .env με το ElephantSQL URL σας

cp ./front-end/.env.sample ./front-end/.env
# ➤ Δεν απαιτείται αλλαγή εκτός αν χρησιμοποιείτε διαφορετικό backend URL

# Βήμα 3: Εγκατάσταση εξαρτήσεων
npm install

# Βήμα 4: Εκκίνηση σε development mode
npm run start:dev 


