Arbeitszeit pro Tag pro Kunde/Projekt

Kunden haben eine oder mehrere Häuser/Adresse
Ein Arbeitstag kann kann bei mehreren Kunden sein

# ER Diagramm
``` java

erDiagram
Customer {
	autonumber id PK
	string FirstName
	string LastName
}

Places {
	string Address
	int ownedBy FK
}

Work {
	autonumber id PK
	dateFormat From
	dateFormat To
	int WorkErrand FK
	int WorkDay FK
}

WorkDay {
	autonumber id
	dateFormat Day
}

WorkErrand {
	autonumber id
	int Work FK
	int WorkType FK
	string Comment
}

WorkType {
	autonumber id PK
	string Name
	string Description
}

Customer ||--|{ Places : owns
Work }|--|{ Places : isDoneAt
Work }|--|{ WorkErrand : has
WorkErrand }|--|{ WorkType : is
WorkDay ||--|{ Work : done
```

![[Projects/Current Projects/WorkTracker/er_diagramm.svg]]