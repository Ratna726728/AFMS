afms/
│
├── .git/
├── .gitignore
├── README.md
│
├── docs/
│   ├── requirements/
│   │   └── requirements.md
│   │
│   ├── architecture/
│   │   ├── architecture.md
│   │   └── diagrams/
│   │
│   ├── environment/
│   │   ├── dev.md
│   │   ├── qa.md
│   │   └── prod.md
│   │
│   ├── database/
│   │   ├── database-design.md
│   │   └── schema.md
│   │
│   ├── development/
│   │   └── development-guide.md
│   │
│   ├── testing/
│   │   ├── test-plan.md
│   │   └── test-cases.md
│   │
│   ├── deployment/
│   │   ├── deployment-guide.md
│   │   └── rollback.md
│   │
│   └── troubleshooting/
│       └── troubleshooting.md
│
├── src/
│   └── main/
│       └── java/
│           └── com/
│               └── afms/
│                   ├── Main.java
│                   │
│                   ├── model/
│                   │   └── Application.java
│                   │
│                   ├── dao/
│                   │   └── ApplicationDAO.java
│                   │
│                   ├── service/
│                   │   └── ApplicationService.java
│                   │
│                   ├── cli/
│                   │   └── ApplicationCLI.java
│                   │
│                   ├── validation/
│                   │   └── InputValidator.java
│                   │
│                   ├── database/
│                   │   └── DatabaseConnection.java
│                   │
│                   └── util/
│                       └── LoggerUtil.java
│
├── src/
│   └── test/
│       └── java/
│           └── com/
│               └── afms/
│                   └── ...
│
├── database/
│   ├── schema/
│   │   ├── 01-create-database.sql
│   │   ├── 02-create-tables.sql
│   │   └── 03-create-users.sql
│   │
│   └── data/
│       └── test-data.sql
│
├── scripts/
│   ├── setup-dev.sh
│   ├── setup-qa.sh
│   ├── setup-prod.sh
│   ├── start.sh
│   └── backup-db.sh
│
├── config/
│   ├── dev/
│   ├── qa/
│   └── prod/
│
└── Vagrantfile
