**PhantomShield/
│
|── main.cpp
|
├── Core/
│   ├── Core.hpp          # Main controller and orchestrator
│   ├── Config.hpp                 # Config and rule sets
│   └── Utils.hpp             # Shared helpers
│
├── Components/
│   ├── ServiceDisabler.hpp        # Detects and disables vulnerable Windows services
│   ├── ServiceSpoofer.hpp         # Launches fake services with fake banners (e.g., SSH, RDP)
│   ├── FirewallBouncer.hpp        # Syncs IPs via Mongo and blocks them locally
│   ├── ProcessSniper.hpp          # Kills dangerous processes instantly
│   └── BlueShell.hpp              # Provides trusted shell interface for defenders only
│
├── Network/
│   └── MongoSync.hpp              # Handles communication with shared IP database
│
├── DefenderUI/
│   └── PhantomCLI.hpp             # C++ shell interface for the blue team (secured, backdoor-proof)
|
├── Build/
│   └── [Compiled binaries, logs, etc.]
│
└── README.md                      # Explains purpose of each component
**
