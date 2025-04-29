**PhantomShield/
│
├── Core/
│   ├── PhantomShield.cpp          # Main controller and orchestrator
│   ├── Config.hpp                 # Config and rule sets
│   └── Utils.cpp/.hpp             # Shared helpers
│
├── Components/
│   ├── ServiceDisabler.cpp        # Detects and disables vulnerable Windows services
│   ├── ServiceSpoofer.cpp         # Launches fake services with fake banners (e.g., SSH, RDP)
│   ├── FirewallBouncer.cpp        # Syncs IPs via Mongo and blocks them locally
│   ├── ProcessSniper.cpp          # Kills dangerous processes instantly
│   └── BlueShell.cpp              # Provides trusted shell interface for defenders only
│
├── Network/
│   └── MongoSync.cpp              # Handles communication with shared IP database
│
├── DefenderUI/
│   └── PhantomCLI.cpp             # C++ shell interface for the blue team (secured, backdoor-proof)
│
├── Build/
│   └── [Compiled binaries, logs, etc.]
│
└── README.md                      # Explains purpose of each component
**
