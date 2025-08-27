# Sources

## Tools

* **Radiation risks that apply to a specific set of circumstances**: <https://vanguard.isde.vanderbilt.edu/RGentic/>
* **NASA electronic parts and packaging**: <https://nepp.nasa.gov/>

## Papers & Presentations

### Radiation

* **OS Dependencies on CPU SEFIs, NASA 2024**: <https://seemapld.org/archive/2024/2024-05-17-Fri/0950-Roffe-2024-SEE-MAPLD-Presentation-20240005835.pdf>
  Linux modifications, "Extend to other Architectures: RISC-V, GPUs and other Accelerators"
* **NASA Radiation Effects and Analysis Group DB**: <https://nepp.nasa.gov/radhome/RadPubDbase/RadPubDbase.html>
* **Future Lunar Surface Network Study, Nokia 2024**: <https://ntrs.nasa.gov/api/citations/20240003815/downloads/NASA%203GPP%20Study%20Final%20Project%20Report%20Consol%20UDR.pdf>

  > "For example, radiation tolerant versions of 3GPP SoC/SiPs do not exist to date, and would
  > require deep IC re-design, using both more resilient processes (like SOI) and/or ah-hoc
  > mitigation techniques (like Error Detection and Correction, memory scrubbing, triple
  > redundancy)."

### Safety

* **Runtime Verification with Ogma, NASA 2023**: <https://ntrs.nasa.gov/api/citations/20230010722/downloads/2023-01-19-Perez-UCSC-RV-with-Ogma-v1.pdf>
* **Lessons Learned and Gaps in Standards Related to Controlling Catastrophic Hazards for Human Spacecraft Propulsion Systems, NASA 2025**: <https://ntrs.nasa.gov/api/citations/20250004573/downloads/Lesson%20Learned%20and%20Prop%20Stand%20TIM%206-13-25%20R3.pdf>
  > Requirement that address a gap in an Existing Standard:
  > * "flight hardware shall be monitored and protected with 1 fault tolerance, against over-pressurization, over-voltage, over current, excessive
  > vibration or shock"
  > * "Detect, isolate and recover from failure modes and hazards identified during system design, development, or mission
  > operations within the time limit necessary to mitigate the catastrophic failure"
  > * "FDIR software shall screen for instrumentation failures that are OSL/OSH and also correct for bias/offsets."
* **Historical Aerospace Software Errors Categorized to Influence Fault Tolerance, NASA 2024**: (future directions section) <https://ntrs.nasa.gov/api/citations/20230012909/downloads/Historical%20Aerospace%20Software%20Errors.pdf>

  > "It is acknowledged that software
  > development tools and practices such as continuous
  > integration have enabled increased productivity and may help
  > ensure higher quality software, however, the author believes
  > that the rate of software/automation growth [11] has offset
  > these practice improvements. As a response to increased
  > volume, software development efforts have had to become
  > more data driven and more configurable -- it simply cannot
  > be rewritten for every configuration or for every flight. It is
  > speculated that errors introduced through configuration data
  > or version management will become more significant with
  > modern software designs, though the overall occurrence of
  > software error incidents will likely continue."
* **Rapid Spacecraft Payload Development: In-Orbit Demonstration of Flight Software Reuse, Scalability, and Dependability, Unibap (competitor) 2024**: <https://ntrs.nasa.gov/api/citations/20230000794/downloads/DSA_SpaceCloud_Payload_Experiment_Paper-2.pdf>, presentation: <https://www.youtube.com/watch?v=pjgIFhgMtPU>

  > "Docker containers for fault tolerance"

* **A System to Provide Deterministic Flight Software Operation and Maximize
Multicore Processing Performance: The Safe and Precise Landing, NASA 2023**: <https://ntrs.nasa.gov/api/citations/20230018685/downloads/SCC2023_8266_Rutishauser_Presentation.pdf>

  > Enable landing at locations that pose significant risk to
  > vehicle touchdown or payload deployment (including
  > near pre-positioned surface assets)

  > Approach was to use embedded Linux OS and develop a datapath
  > that isolates the application processors from interrupts associated
  > with the sensor I/O to support deterministic operation.

* **NOR Flash Memory Scrubbing Application for Boot File
Preservation of NASA’s Descent and Landing Computer (DLC), NASA 2021**: <https://ntrs.nasa.gov/api/citations/20210016267/downloads/NOR_Flash_Memory_Scrubbing_Application_for_DLC.pdf>

* **Verification and Validation of
the OS for NASA, 2024**: <https://ntrs.nasa.gov/api/citations/20240015845/downloads/2024%20ELISA_VV_Certpackage.pdf>

  > Short guideline for safety-critical software

### Operating Systems

* **CubedOS: A Verified CubeSat Operating System, Vermont Technical College 2017**: <http://lemuria.cis.vermontstate.edu/CubeSat/PUBLIC/brandon-chapin-farnsworth-klink-AUJ-2017.pdf>, repo: <https://github.com/cubesatlab/cubedos>

  > CubedOS is
  > written entirely in SPARK and proved free of runtime errors
  > in the sense meant by SPARK.
  > CubedOS provides a great deal of concurrency and runtime
  > flexibility, but sacrifices some static type safety to achieve this. We mitigate the danger using a tool, XDR2OS3, that
  > generates message encoding and decoding subprograms based
  > on strongly typed message descriptions. The output of the
  > tool is verified by SPARK.

* LynxOS modifications: **Flight Software for the LOFTID Re-Entry Vehicle, NASA 2023**: <https://ntrs.nasa.gov/citations/20230002320>

  > Based on posix OSAL and pc-linux PSP
  
  > OSAL
  > * Threaded Signal Handler behavior ambiguity
  > * POSIX does not define which thread receives a given signal
  > * Created dedicated Timer Thread to do signal handling
  > * Used msg queue for other threads to add and remove signals
  > * Pthread Mutexes were not recursive
  > * Added recursive functionality to OS_mutex
  > * Dynamic Object Loader API inconsistent
  > * Switched to using a module id for all shared object symbol lookups

  > PSP
  > * Shared Memory inconsistent
  > * Switched to POSIX real-time shared memory
  > * Reworked Timer Thread to reflect OSAL changes

### Misc

* **Space Based Solar Power, NASA 2024**: <https://ntrs.nasa.gov/api/citations/20230018600/downloads/OTPS%20SBSP%20Report%20Final_Tagged_Approved_1_5_24.pdf>
  Lots of future directions
* **Standards and Schematics for Intelligent Extensible Mission Architectures in Space, NASA 2025**: <https://ntrs.nasa.gov/api/citations/20250005873/downloads/DASS-Camera-Ready.pdf>

  > "Additionally, incrementing infrastructure in space
  > to build large space weather networks will provide alerts to
  > astronauts exploring the surface of the Moon and Mars.
  > Similarly, incrementing assets observing deep-space planetary
  > environments on an “as needed” basis will enable multi-shot
  > observation of possible life on other planetary bodies like
  > Enceladus and Europa. This is particularly important in
  > communication limited environments of planetary exploration.
  > Lastly, being able to capture celestial events by connecting
  > large telescopes and observatories through responsive obser-
  > vation will unlock insights into universe formation questions
  > and habitable worlds"

* **Rapidly Deployable Satellite-Based Emergency Communications Infrastructure, Swinburne University of Technology, Melbourne 2024**: <https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=10685402>

  > * Our
  > comprehensive analysis reveals a gap in addressing interoperability issues caused by disparate communica-
  > tion standards, processing power and energy requirements. Further analysis reveals promising open-source
  > initiatives that offer potential solutions, such as low-data rate modulation schemes, low-bitrate voice
  > codecs, and low-power encryption techniques.
  > * Future work
  > should leverage advancements in low-bitrate technologies to enhance emergency systems, ensuring secure
  > and resilient two-way voice, messaging, and distress signalling capabilities for critical communications.
  > * Recent research identifies the potential of the Medium
  > Earth Orbit Search and Rescue (MEOSAR), which provides
  > a highly available 406MHz emergency communication
  > channel with restricted services. For instance, novel work that
  > leverages advances in SDR and satellite waveform technolo-
  > gies demonstrates the reuse of existing MEOSAR resources

* **The Design of a Flexible, Interoperable Navigation Signal for Future Lunar Missions, NASA 2025**: <https://ntrs.nasa.gov/citations/20250000725>

  > The LunaNet Interoperability Specification (LNIS) is a set of standards currently under development by NASA, ESA, and JAXA, which define a common, interoperable set of services and interfaces for
  > lunar communication and navigation. The LNIS includes specifications for the GNSS-like Augmented Forward Signal (AFS).

* **Cold Electronics for Lunar Missions, NASA 2025**: <https://ntrs.nasa.gov/api/citations/20250008583/downloads/20250008583.pdf>

  > no cold capable avionics architecture meeting requirements like those of lunar
  > surface missions has yet been fully implemented. Studies and technology readiness level (TRL)
  > 32 prototypes show the feasibility of such an architecture, but none has yet been fully built,
  > qualified, or fielded.

  > Microcontrollers and field programmable gate arrays (FPGAs) are important to run the system or
  > spacecraft, and COTS/MIL testing reveals that many COTS/MIL FPGAs start to behave poorly
  > at temperatures as high as -123 °C (150 K). There are some candidates such as the Artix7 FPGA,
  > which seem to have good performance down to -269 °C (4 K) except for increased jitter

  > SiGe is an alternative that has reliable performance at extremely low temperatures. SiGe exploits
  > HBTs which are not prone to hot carrier damage. Fairly complex IC can be rendered in SiGe.

  > Once avionics are warmed up to operating temperatures, the MBC then begins methodically
  > activating the power distribution system to power up the avionics. The highest priorities are mission dependent but are likely to be the radio transmitter, flight computer, and data network.
  > With the flight computer active, the power management can be taken over by a software module
  > in the flight computer. With the data system, flight computer and RF communications
  > reestablished the spacecraft can resume interaction with mission control as necessary for the
  > mission.

* **Highly-miniaturized spacecraft “PlanarSat”: Evaluating prospects and challenges through
a survey of femto & atto satellite missions, TUDelft 2025**: <https://pure.tudelft.nl/ws/portalfiles/portal/249293307/1-s2.0-S0094576525003005-main.pdf>

  > Monarch,
  > with a mass of 5 grams and dimensions of 5 × 5 cm2, is a printed
  > circuit board on a kapton substrate. They are designed to be deployed
  > in large batches form a mothership and create a swarm to collect data
  > from multiple locations simultaneously. Monarch’s first launch
  > opportunity is planned as a part of a solar sail, Alpha Sail developed
  > by Cornell University. Four Monarchs would be placed, two on each
  > face of the sail. This mission was designed, to test the effectiveness of
  > a highly reflective material intended for light-sail propulsion

  > POQUITO attosatellite network: demonstrate
  > an LED-based communication in between attosatellites to transmit their
  > data. The network’s primary element can transmit data via its RF
  > transmitter

  > Although studies highlight
  > the potential for swarm applications of femto/attosatellites, they do
  > not specify the required number of satellites, as these missions are not
  > yet planned and the studies primarily focus on the satellite technology
  > itself.

  > lack of dedicated launchers/deployers for PlanarSat => contradicting concerning mission cost, especially when the launch is included.

  > Photonic propulsion, such as laser and solar sails, offers propellant-less solutions which might be ideal for PlanarSats

  > Lubin’s research into directed energy propulsion explores wafer-scale spacecraft accelerated to relativistic speeds by phased laser arrays, presenting opportunities for interstellar probes and LEO missions alike
  
  > PlanarSats stand out in distributed applications, providing unique cost–effective opportunities to enhance spatial and temporal resolution, making them ideal for complex, multi–point measurement tasks that larger satellites cannot perform as efficiently.

  > Asteroid mining

## ESA Handbooks

* <https://ecss.nl/hbs/active-handbooks/>
