# Επίμονη PvP Εκστρατεία στη Συρία

## Γιατί μια νέα αποστολή;

Επειδή αυτή η αποστολή προσπαθεί να λύσει τα παρακάτω προβλήματα:

- **Νοοτροπία άπειρων αεροσκαφών**  
  Τα περιορισμένα airframes κάνουν τη διατήρηση των αεροσκαφών σημαντική. Οι παίκτες πρέπει να επιστρέφουν στη βάση αντί να αντιμετωπίζουν τα jet σαν αναλώσιμους πυραύλους με cockpit.

- **Αίσθηση άπειρων όπλων**  
  Δεν υπάρχει συνεχές γέμισμα της αποθήκης όπλων. Τα αεροπορικά όπλα γίνονται περιορισμένα και αναπληρώνονται αργά, πιθανώς εβδομαδιαία.

- **Το fuel να μην έχει νόημα**  
  Τα refineries και τα fuel stocks γίνονται strategic assets. Το fuel υποστηρίζει τις πτήσεις, τη λειτουργία των airfields και την αντικατάσταση airframes.

- **Βαρετή στατική γραμμή μετώπου**  
  Οι μεγάλες POI zones δημιουργούν φυσικούς στόχους εκστρατείας στο κέντρο του χάρτη.

- **Χάος σε όλο τον χάρτη**  
  Red και Blue ξεκινούν σε περιορισμένες περιοχές, με μια κεντρική contested ζώνη. Η μάχη αποκτά σχήμα.

- **Πάρα πολλοί μικροί στόχοι**  
  Λιγότερες και μεγαλύτερες ζώνες μειώνουν τον θόρυβο και κάνουν κάθε objective άξιο σχεδιασμού.

- **Το παράλογο όπου ένα φορτηγό καταλαμβάνει ολόκληρο refinery**  
  Υψηλές τιμές `numCap` και `numKeep` επιβάλλουν σοβαρή δέσμευση χερσαίων δυνάμεων.

- **Εύκολη αλλαγή ιδιοκτησίας ζώνης**  
  Το `easyContest = false` κάνει τα captured POIs πιο δύσκολο να ουδετεροποιηθούν ή να αλλάξουν χέρια πρόχειρα.

- **Κυριαρχία αποκλειστικά αεροπορικού gameplay**  
  Ground commanders, convoys, armor, IFVs, SHORAD και ελικόπτερα αποκτούν πραγματική σημασία.

- **Οι ground commanders να μην έχουν ουσιαστικό ρόλο**  
  Συγκροτούν produced units, ενισχύουν POIs, μετακινούν convoys, προστατεύουν logistics και υποστηρίζουν captures.

- **Factories που παράγουν γενικά τα πάντα**  
  Specialized factories κάνουν συγκεκριμένες περιοχές στρατηγικά σημαντικές: tank factory, IFV factory, SHORAD factory, radar factory κ.λπ.

- **Κανένας λόγος να πολεμάει κάποιος για συγκεκριμένες περιοχές**  
  Κάθε POI δίνει συγκεκριμένο όφελος. Οι ομάδες θα πολεμούν για αυτό που χρειάζονται, όχι απλώς για ό,τι βρίσκεται κοντά.

- **Airfields που καταλαμβάνονται απλώς για να βαφτεί ο χάρτης**  
  Τα airfields είναι consumers. Είναι χρήσιμα μόνο αν τροφοδοτούνται και προστατεύονται.

- **Forward bases που γίνονται μαγικά αυτοσυντηρούμενα νησιά**  
  Ένα captured airfield χωρίς fuel, aircraft και logistics είναι liability, όχι win button.

- **Home-base rush cheese**  
  Τα home bases είναι πολύ καλά αμυνόμενα και στρατηγικά σημαντικά, αλλά δεν είναι εύκολοι στόχοι κατάληψης.

- **Parked aircraft ως άχρηστο scenery**  
  `StopGap` + `SittingDucks` κάνουν τα parked aircraft πραγματικούς στόχους. Ramp strikes μπορούν να μειώσουν την εχθρική αεροπορική ισχύ.

- **Καμία συνέπεια για κακές αποφάσεις πιλότων**  
  Η απώλεια aircraft επηρεάζει ολόκληρο το coalition inventory.

- **Καμία δυνατότητα ανάκαμψης μετά από απώλειες aircraft**  
  Το fuel-for-airframes επιτρέπει ανάκαμψη, αλλά μόνο μέσω strategic fuel surplus και delayed delivery.

- **Arcade συμπεριφορά άμεσης αντικατάστασης**  
  Τα purchased aircraft φτάνουν αργότερα, όχι αμέσως.

- **Refineries ως διακοσμητικά map objects**  
  Γίνονται fuel-production nodes και έμμεσα airpower-recovery nodes.

- **Recon ως προαιρετικό fluff**  
  Το Recon Mode κάνει helicopters, scouts και recon aircraft χρήσιμα για εντοπισμό convoys, defenses και αδύναμων POIs.

- **Τα helicopters να μην έχουν στρατηγικό ρόλο**  
  Chinooks, Hueys, Kiowas κ.λπ. γίνονται χρήσιμα για capture support, troop movement, recon και logistics.

- **SHORAD και radar assets που εμφανίζονται μαγικά**  
  Παράγονται αργά από συγκεκριμένα factories, κάνοντας το air-defense buildup σκόπιμο και σταδιακό.

- **Υπερβολικό message spam**  
  Τα live messages μένουν ελάχιστα. Πιο αναλυτικό status μπορεί να ζητείται μέσω F10.

- **Υπερβολικό χτίσιμο με custom static objects**  
  Μπορούν να χρησιμοποιηθούν τα υπάρχοντα Syria map assets. Οι DML zones παρέχουν τη λογική του παιχνιδιού.

- **Η αποστολή να γίνει script soup πολύ νωρίς**  
  Το DML χειρίζεται ownership, factories, recon, parked aircraft και messaging. Μόνο το fuel-for-airframes mechanic πιθανότατα χρειάζεται ένα μικρό custom script.

- **Έλλειψη campaign economy**  
  Το design δημιουργεί ξεχωριστές οικονομίες: fuel, airframes, ground vehicles και strategic factories.

- **Έλλειψη στρατηγικής επιλογής**  
  Οι ομάδες πρέπει να αποφασίσουν αν θα ξοδέψουν fuel για πτήσεις, αν θα το κρατήσουν για aircraft replacement, αν θα χτυπήσουν refineries, αν θα υπερασπιστούν factories ή αν θα πιέσουν προς airfields.

- **Το PvP να γίνεται απλώς CAP vs CAP**  
  Το CAP παραμένει σημαντικό, αλλά πλέον υποστηρίζει πραγματικούς στρατηγικούς στόχους: προστασία convoys, δυνατότητα captures, άμυνα refineries και αναχαίτιση strikes.

- **Μικρή μοίρα που απλώνεται υπερβολικά**  
  Λιγότεροι μεγάλοι στόχοι συγκεντρώνουν τη μάχη σε κατανοητές περιοχές.

- **Η πρόοδος της αποστολής να μοιάζει αφηρημένη**  
  Η πρόοδος φαίνεται: captured POIs παράγουν resources, airfields γίνονται usable, aircraft inventories μειώνονται ή ανακάμπτουν.

- **Έλλειψη επιχειρησιακής ταυτότητας**  
  Η αποστολή γίνεται combined-arms logistics war, όχι απλώς τυχαίες εξόδοι σε έναν μεγάλο χάρτη.

---

Μια επίμονη multiplayer PvP αποστολή για το **DCS World** στον χάρτη **Syria**.

Η αποστολή είναι σχεδιασμένη ως επιχειρησιακή εκστρατεία, όχι ως απλό front-line brawl. Red και Blue ξεκινούν με περιορισμένες αλλά καλά εξοπλισμένες home areas. Ανάμεσά τους υπάρχει μια contested ζώνη με σημαντικά οικονομικά και στρατιωτικά σημεία ενδιαφέροντος: refineries, ports, vehicle factories, radar production sites, armored depots, SHORAD depots και forward airfields.

Η εκστρατεία περιστρέφεται γύρω από την κατάληψη, τη διατήρηση, την τροφοδοσία, την άμυνα και την καταστροφή αυτών των assets.

Η βασική αρχή είναι απλή:

> Η αεροπορική ισχύς κερδίζει μάχες, τα logistics κερδίζουν εκστρατείες, και οι απρόσεκτοι πιλότοι μετατρέπουν ακριβά aircraft σε αλουμινένιο κομφετί.

---

## Mission Concept

Red και Blue ξεκινούν με ένα μικρό, ασφαλές μέρος του χάρτη. Η κεντρική περιοχή περιέχει μεγάλες strategic POI zones. Αυτές οι ζώνες δεν είναι απλώς διακοσμητικά objectives. Καθορίζουν fuel supply, ground vehicle production, τη χρησιμότητα των airfields και το momentum της εκστρατείας.

Οι παίκτες και οι ground commanders πρέπει να πολεμήσουν για να ελέγξουν αυτά τα assets και μετά να τα χρησιμοποιήσουν για να επεκταθούν στον χάρτη.

Η αποστολή προορίζεται να τρέχει συνεχώς σε multiplayer server.

---

## Design Goals

- Δημιουργία persistent PvP campaign στον χάρτη Syria.
- Αποφυγή full-map chaos μέσω περιορισμένου αριθμού μεγάλων strategic zones.
- Να γίνουν aircraft και pilots πολύτιμα μέσω finite airframes και vulnerable parked aircraft.
- Να έχουν σημασία τα logistics και οι ground commanders.
- Να ενθαρρυνθεί planning, reconnaissance, convoy assembly, interdiction, escort, SEAD, CAS και strategic strikes.
- Αποφυγή infinite-weapons και magic-warehouse behavior.
- Χρήση DML zones και map-native assets όπου είναι δυνατό, αντί για χειροκίνητο χτίσιμο κάθε site με static objects.
- Χρήσιμα αλλά όχι ενοχλητικά messages και player feedback.
- Πρώτα playable v1, μετά επέκταση με persistence και automation.

---

## Core Gameplay Loop

```text
Οι παίκτες πετούν αποστολές
        ↓
Το recon εντοπίζει εχθρικές μονάδες και αδύναμα σημεία
        ↓
Strikes, CAS και ground commanders διαμορφώνουν τη μάχη
        ↓
Οι χερσαίες δυνάμεις καταλαμβάνουν μεγάλες strategic zones
        ↓
Owned factories και refineries αρχίζουν να παράγουν resources
        ↓
Convoys και logistics συντηρούν airfields και forward positions
        ↓
Τα coalitions επεκτείνονται μόνο όπου μπορούν να υποστηρίξουν operations
```

---

## Main Campaign Mechanics

### 1. Limited Airframes

Και τα δύο coalitions έχουν finite pool διαθέσιμων aircraft.

Η διαθεσιμότητα aircraft βασίζεται στον αριθμό των squadron members που έχουν κάθε module, όχι μόνο σε όσους αναμένεται να πετάξουν μια συγκεκριμένη Κυριακή. Οι αριθμοί μπορούν να ληφθούν από το Discord channel `MyModules`.

Παράδειγμα αρχικού inventory concept:

| Airframe | Example count |
|---|---:|
| F-16C | 56 |
| F/A-18C | 48 |
| F-4E | TBD |
| F-5E | TBD |
| Mirage 2000C | TBD |
| Mirage F1 | TBD |
| UH-1H | TBD |
| AH-64D | TBD |
| CH-47F | TBD |
| OH-58D | TBD |

Η διατήρηση των aircraft είναι κεντρική στην αεροπορική εκστρατεία.

Τα aircraft δεν είναι disposable. Μια επιτυχημένη αποστολή δεν αφορά μόνο την καταστροφή στόχων, αλλά και την επιστροφή του aircraft στη βάση.

---

### 2. Parked Aircraft and Airbase Vulnerability

Η αποστολή πρέπει να χρησιμοποιεί:

- `StopGap`
- `SittingDucks`
- `Valet`

Ο σκοπός:

| DML module | Intended use |
|---|---|
| `StopGap` | Γεμίζει empty client slots με ορατά parked aircraft stand-ins. |
| `SittingDucks` | Κάνει τα parked stand-ins vulnerable, ώστε destroyed aircraft να μπορούν να μπλοκάρουν αντίστοιχα slots. |
| `Valet` | Παρέχει airbase/FARP entry, departure, greeting και base-status behavior. |

Αυτό επιτρέπει στα airbases να γίνουν meaningful targets χωρίς τεχνητούς scoring rules.

Ένα επιτυχημένο ramp strike μπορεί να μειώσει τα διαθέσιμα airframes του αντιπάλου.

Τα home bases είναι heavily defended και well equipped, αλλά δεν πρέπει να είναι εντελώς immune σε enemy action.

---

### 3. Strategic POI Zones

Η κεντρική ζώνη του χάρτη περιέχει μεγάλες strategic zones.

Αυτές δεν είναι μικροί κύκλοι γύρω από ένα αντικείμενο. Μια refinery zone μπορεί να περιλαμβάνει:

- refinery
- tank farm
- harbor
- loading area
- nearby road/rail access
- associated defensive positions

Το coalition πρέπει να ελέγχει ολόκληρη την operational area, όχι απλώς να παρκάρει ένα όχημα δίπλα σε ένα fuel tank.

Παραδείγματα strategic zones:

| Zone type | Example effect |
|---|---|
| Oil refinery + port | Παράγει fuel για owned και supported airfields. |
| APC factory | Παράγει APCs ή troop carriers. |
| IFV factory | Παράγει infantry fighting vehicles. |
| Tank factory | Παράγει tanks με πιο αργό ρυθμό. |
| SHORAD factory | Παράγει short-range air defense units. |
| Radar factory | Παράγει EWR/search radar assets πολύ αργά. |
| Forward airfield | Γίνεται χρήσιμο μόνο αν supplied. |

---

### 4. Zone Capture Rules

Η κατάληψη ενός POI πρέπει να απαιτεί σοβαρή χερσαία δύναμη.

Προτεινόμενες αρχικές τιμές:

| Zone type | `numCap` | `numKeep` |
|---|---:|---:|
| Factory / depot | 8-10 | 4-5 |
| Refinery + port complex | 10 | 5 |
| Forward airfield | 12-16 | 6-8 |
| Home base | Not normally capturable | N/A |

Προτεινόμενη DML συμπεριφορά:

```text
easyContest = false
```

Λόγος:

Μια ζώνη δεν πρέπει να γίνεται neutral μόνο και μόνο επειδή μπαίνει μέσα ένα εχθρικό scout. Όταν ένα coalition καταλάβει refinery, factory ή port complex, ο εχθρός πρέπει να φέρει αρκετή δύναμη για να το πάρει πραγματικά.

Το προτιμώμενο capture model είναι:

```text
Αρκετές attacking ground units μπαίνουν στη ζώνη
Δεν παραμένει επαρκής defending force
Η ζώνη αλλάζει owner
Ο νέος owner πρέπει να αφήσει αρκετές μονάδες πίσω για να την κρατήσει
```

Tanks, IFVs, APCs, infantry και άλλες ground units μπορούν όλες να συνεισφέρουν στο capture, αλλά η αμυντική διάταξη πρέπει να κάνει απαραίτητο το σωστό force composition.

---

### 5. Refineries and Fuel

Τα oil refineries είναι major strategic assets.

Το fuel πρέπει να παράγεται συνεχώς και να παραδίδεται περιοδικά.

Προτεινόμενος κανόνας:

```text
Oil refinery owned by coalition
        ↓
Fuel is added every 2 hours
        ↓
Only airfields owned and supported by the same coalition receive fuel
```

Αν το refinery είναι neutral ή unsupported, η ροή fuel σταματά.

Προτεινόμενη λογική:

| Refinery owner | Effect |
|---|---|
| Blue | Τα Blue-supported airfields λαμβάνουν fuel. |
| Red | Τα Red-supported airfields λαμβάνουν fuel. |
| Neutral | Κανένα coalition δεν λαμβάνει fuel. |

Τα airfields είναι consumers. Αποκτούν αξία μόνο όταν το coalition μπορεί να τα υποστηρίξει.

---

### 6. Factories Instead of Generic Warehouses

Αυτή η αποστολή δεν χρησιμοποιεί generic warehouse που παράγει κάθε τύπο μονάδας.

Αντίθετα, τα factories είναι specialized.

Ο σκοπός είναι να γίνουν συγκεκριμένες γεωγραφικές τοποθεσίες στρατηγικά σημαντικές.

Παράδειγμα:

| Factory | Produces |
|---|---|
| APC Factory | APCs / troop transports |
| IFV Factory | BMP / Bradley-type vehicles |
| Tank Factory | Main battle tanks |
| SHORAD Factory | Short-range air defense |
| Radar Factory | EWR/search radar assets |
| Logistics Depot | Trucks and support vehicles |

Αυτό δημιουργεί φυσικά focal points για combat.

Ένα coalition που θέλει tanks πρέπει να καταλάβει και να κρατήσει το tank factory. Ένα coalition που θέλει καλύτερη mobile air defense πρέπει να καταλάβει και να κρατήσει το SHORAD factory.

Οι ground commanders μετά συγκροτούν convoys από τα οχήματα που παράγονται από διαφορετικά factories.

---

### 7. Production Tempo

Η παραγωγή πρέπει να είναι αρκετά αργή ώστε να έχει σημασία.

Προτεινόμενες αρχικές τιμές:

| Asset type | Suggested production interval |
|---|---:|
| Infantry / trucks | 1-2 hours |
| APCs | 2 hours |
| IFVs | 3-4 hours |
| Tanks | 6-12 hours |
| SHORAD | 6-12 hours |
| Radar assets | 24-48 hours |
| Aircraft weapons | Weekly delivery, not continuous |

Τα aircraft weapons δεν πρέπει να αναγεννιούνται κάθε 2 ώρες. Αυτό δημιουργεί αίσθηση infinite-weapons.

Αντίθετα:

```text
Fuel = continuous logistical flow
Ground vehicles = industrial production
Aircraft weapons = scarce strategic stock, replenished weekly
```

---

### 8. Ground Commanders

Οι ground commanders αναμένεται να έχουν ουσιαστικό ρόλο.

Πρέπει να:

- assemble convoys
- decide where produced units go
- protect logistics movements
- reinforce captured POIs
- prepare attacks on enemy POIs
- request air support
- coordinate with helicopter transport and reconnaissance assets

Η εκστρατεία πρέπει να ενθαρρύνει πραγματικό combined arms coordination.

---

### 9. Airfields as Consumers

Τα airfields δεν είναι αυτόματα χρήσιμα απλώς επειδή καταλήφθηκαν.

Ένα airfield γίνεται operationally valuable μόνο όταν έχει:

- fuel
- aircraft
- ground security
- supply route
- air defense
- usable logistics link
- sufficient reason to expand in that direction

Προτεινόμενος κανόνας:

```text
Airfield owned + supplied = usable forward base
Airfield owned + unsupported = vulnerable liability
```

Αυτό αποτρέπει τις ομάδες από το να καταλαμβάνουν airfields απλώς για να βάφουν τον χάρτη.

---

### 10. Home Bases

Τα home bases ξεκινούν well equipped και heavily defended.

Πρέπει να έχουν:

- aircraft inventory
- fuel stock
- weapon stock
- SAM/SHORAD protection
- CAP support
- EWR/GCI coverage
- parked aircraft vulnerability
- strong defensive ground units

Πρέπει να είναι δυνατό να δεχτούν επίθεση, αλλά με μεγάλο στρατιωτικό κόστος και ρίσκο.

Το ownership των home bases μάλλον δεν πρέπει να αλλάζει εύκολα, αν αλλάζει καθόλου.

---

### 11. Reconnaissance

Το reconnaissance είναι σημαντικός ρόλος αποστολής.

Η αποστολή πρέπει να χρησιμοποιεί DML `Recon Mode`.

Προτεινόμενα recon-capable assets:

- OH-58D
- UH-1H
- CH-47F
- scout ground vehicles
- possible special recon aircraft roles

Το recon πρέπει να βοηθά στον εντοπισμό enemy ground units, factory outputs, convoy movement και weakly defended POIs.

Το recon δεν πρέπει να αντικαθιστά το tactical flying. Πρέπει να δίνει αρκετές πληροφορίες ώστε το planning να έχει νόημα.

---

### 12. Player Messaging

Τα messages πρέπει να είναι restrained.

Κατά την ανάπτυξη και το debugging, τα verbose messages είναι αποδεκτά.

Στο live play, τα messages πρέπει να είναι ελάχιστα:

- POI captured
- POI lost
- POI neutralized
- factory production completed
- fuel delivery completed
- major airfield supply state changed

Προτιμώμενα live examples:

```text
BLUE captured Baniyas Refinery.
RED captured Hama Tank Factory.
Baniyas Refinery is neutral. Fuel production stopped.
BLUE fuel delivery completed at Incirlik.
```

Αποφυγή constant spam.

Πιο αναλυτικό status information πρέπει να είναι διαθέσιμο μέσω F10 menu ή status report, όχι μέσω συνεχών automatic messages.

---

## DML Module Plan

Η αποστολή είναι σχεδιασμένη γύρω από το DML.

Προβλεπόμενα DML modules:

| Module | Purpose |
|---|---|
| `ownedZones` | Strategic POI ownership. |
| `factoryZones` | Ground vehicle production tied to zone ownership. |
| `Limited Airframes` | Coalition airpower pressure και aircraft/pilot scarcity. |
| `StopGap` | Visible empty aircraft slots. |
| `SittingDucks` | Destructible parked aircraft και slot denial. |
| `Valet` | Airbase/FARP entry και departure behavior. |
| `Recon Mode` | Reconnaissance gameplay για helos, scouts και selected aircraft. |
| `airfield` / `baseCaptured` | Airfield ownership tracking. |
| `messenger` | Controlled player notifications. |
| `wiper` | Cleanup of destroyed units/debris για MP performance. |
| `persistence` | Later phase: save campaign state. |
| `WHpersistence` | Later phase: warehouse/resource persistence αν χρησιμοποιηθεί. |

---

## DML Zone Design

Το DML χρησιμοποιεί Mission Editor trigger zones με attributes.

Τυπική strategic POI zone:

```text
Zone name: POI_BANIYAS_REFINERY_COMPLEX

owner = neutral
numCap = 10
numKeep = 5
easyContest = false
ownedBy# = BaniyasRefineryOwner
redCap! = BaniyasRefineryRed
blueCap! = BaniyasRefineryBlue
neutral! = BaniyasRefineryNeutral
```

Τυπική specialized factory zone:

```text
Zone name: POI_HAMA_TANK_FACTORY

owner = neutral
numCap = 10
numKeep = 5
easyContest = false
ownedBy# = HamaTankFactoryOwner

factory = true
productionRED =
productionBLUE =
```

Τα actual production attributes και templates θα οριστούν στη φάση υλοποίησης της αποστολής.

---

## Proposed v1 Scope

Ξεκινάμε μικρά και κάνουμε το core loop να δουλέψει.

Προτεινόμενο v1:

| Item | Count |
|---|---:|
| Blue home base | 1 |
| Red home base | 1 |
| Large strategic POI zones | 5-7 |
| Refineries | 1-2 |
| Vehicle factories | 3-4 |
| Forward airfields/FARPs | 1-2 |
| Recon roles | enabled |
| Limited airframes | enabled |
| StopGap/SittingDucks | enabled |
| Full persistence | later |
| Logistics hub repair system | skipped for v1 |
| Generic weapon warehouses | skipped for v1 |

---

## Proposed Strategic POIs

Αρχικοί υποψήφιοι τύποι:

1. Refinery + port complex
2. APC factory
3. IFV factory
4. Tank factory
5. SHORAD factory
6. Radar factory
7. Forward airfield or logistics town

Οι ακριβείς τοποθεσίες θα επιλεγούν στον χάρτη Syria με βάση terrain, existing map assets, road access, airfield placement και playability.

---

## Persistence Plan

Το persistence είναι σημαντικό, αλλά δεν απαιτείται για το πρώτο λειτουργικό prototype.

Το Phase 1 πρέπει να εστιάσει στα εξής:

- zone ownership
- capture behavior
- aircraft vulnerability
- factory production
- fuel supply
- player feedback

Σε επόμενες φάσεις μπορούν να γίνουν persist:

- zone ownership
- aircraft losses
- blocked slots
- factory stock/output
- fuel levels
- convoy state
- warehouse/resource state

---

## Implementation Philosophy

Χτίζουμε την εκστρατεία σε layers.

1. Κάνουμε το ownership να δουλέψει.
2. Κάνουμε το capture δύσκολο και ουσιαστικό.
3. Κάνουμε τα factories να παράγουν τις σωστές ground unit classes.
4. Κάνουμε το fuel supply να επηρεάζει τα airfields.
5. Προσθέτουμε limited aircraft και parked-aircraft vulnerability.
6. Προσθέτουμε recon.
7. Προσθέτουμε persistence μόνο αφού δουλέψει το gameplay loop.

Αποφεύγουμε να χτίσουμε έναν τεράστιο αόρατο μηχανισμό πριν διασκεδάσει ο πρώτος παίκτης.

---

## Current Status

Initial concept and design phase.

Δεν έχει οριστεί ακόμα final mission file structure.

Δεν περιλαμβάνονται production scripts σε αυτό το README.

---

## Notes for Mission Designers

- Χρησιμοποιήστε existing Syria map assets όπου είναι δυνατό.
- Χρησιμοποιήστε large zones για operational complexes, όχι tiny capture circles.
- Μην κάνετε κάθε POI να παράγει τα πάντα.
- Μην κάνετε over-message τους παίκτες.
- Κρατήστε τα home bases strong αλλά όχι πλήρως magical.
- Κάντε το aircraft preservation να έχει σημασία.
- Κάντε τα logistics meaningful.
- Κάντε τους ground commanders useful.
- Κρατήστε την πρώτη έκδοση playable πριν προσθέσετε περισσότερη μηχανή.

---

## License

TBD.

---

## Credits

Mission concept and design: Lock-On Greece

Built for DCS World using DML by cf/x.
