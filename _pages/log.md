---
layout: default
title: IMMERSE Log
---

### Week 1: April 26, 2021

* **Monday**:    Moved to a new apartment.
* **Tuesday**:   Moved to a new apartment.
* **Wednesday**: Set up computer and website, completed linux tutorial, and attened immerse meetings.
* **Thursday**:  Set up and experimented with VTR, attended VTR meeting, upgraded Linux, and compared 
                 the FPGA implementation in VTR and Vivado.
* **Friday**:    Read about VTR Architecture xml files and created a custom architecture by copying an 
                 existing architecture and modifying it. Attended bootcamp meeting about github.

### Week 2: May 3, 2021

* **Monday**:   Created an XML Architecture Template that explains necessary commands and includes 
                examples. Experimented with architecture layouts and attended bootcamp meeting about VSCode.
* **Tuesday**:  Read about what Netcracker revealed about Xilinx FPGA routing and studied Xilinx FPGA 
                implemented design. Created a new architecture from my template and experimented with different designs.
* **Wednesday**: Continued to study Xilinx architecture and compare it with VPR designs. Completed
                 assignments for Ethics group. Attended immerse meetings.
* **Thursday**: In-depth study of Xilinix architecture. Attended meeting about VTR project. Worked on 
                assignment for Ethics group.
* **Friday**: Continued in-depth study of Xilinix architecture and read about FPGA routing. Attended 
              bootcamp meeting about cmake.

### Week 3: May 10, 2021

* **Monday**:   Assembled a verilog program in VTR and studied the primitives in the symbiflow arch def 
                project. Attended bootcamp meeting about python and wrote several small python scripts to practice.
* **Tuesday**:  Adjusted my website and added myself to the CCL website. Fixed several small bugs in 
                VTR architecture files, improved one of my python scripts, and studied more about FPGA architecture.
* **Wednesday**: Created the csv_parser python script and attended immerse meetings. Also made another
                 small adjustment to my website and updated git repositories.
* **Thursday**: Read about Xilinx primitives and compared them to the symbiflow_arch_defs xml files. 
                Attended meeting about VTR, wrote a python script to convert tab delinieated .txt files to comma 
                deliniated .csv files, and ran some regression tests.
* **Friday**: Ran regression tests to comapre modified versions of VTR architectures to their originals, 
              attended bootcamp meeting about python packages, and experimented with the packages.

### Week 4: May 17, 2021

* **Monday**: Ran additional regression tests on modified files and attended bootcamp about unit tests 
              and github actions. Also wrote summer proposal.
* **Tuesday**: Made modifications to a test architecture to make it mirror the Vivado architecture 
               layout. Ran regression tests on various designs and also worked on a CVS finder python script.
* **Wednesday**: Added additional clock regions to the test architecture, attended immerse meetings, and 
                 experimented with pylint and sphinx.
* **Thursday**: Worked more on the test architecture and examined switchblock connections in VTR. 
                Attended VTR meeting and started reading about how to use Netcracker.
* **Friday**: Started working on project presentation, attended bootcamp meeting about docker, and read 
              more about how to use Netcracker.

### Week 5: May 24, 2021

* **Monday**: Completed project presentation, attended FPGA overview meeting, and compared different
              Artix-7 architectures. Also set up an xserver on my laptop so I can work remotely.
* **Tuesday**: Reviewed project presentation and experimented with routing settings in VTR. Finally 
               got second monitor to work and wrote down questions for our next VTR meeting.
* **Wednesday**: Attended immerse meetings and gave my presentation about VTR. Experimented more with
                 VTR routing and wrote down additional questions.
* **Thursday**: Continued to experiment with routing in VTR. Attended VTR meeting and began to experiment
                with changing the rr_graph.cpp code to accomodate different channel widths.
* **Friday**: Worked on case study analysis for ethics broader impacts group and self-paced Xilinx FPGA
              deep dive activities. Also studied several VTR cpp files and attempted to make changes
              to allow for custom channel width.

### Week 6: May 31, 2021

* **Monday**: Memorial Day Holiday.
* **Tuesday**: Read through more of the VTR code to understand it and tried to learn more about
               the channel widths. Also worked more on my ethics case study analysis and experimented
               with CMake, gitignore, and my test code. 
* **Wednesday**: Experimented with the different types of routing options in VTR and attended immerse
                 meetings. Also attended bootcamp meeting about project xray, fasm, and FPGA tools. 
                 Discovered that global routing can be accomplished by setting the --route_type VPR
                 property to global and that the regression testing breaks for some designs due to
                 tests trying odd numbers for channel widths.
* **Thursday**: Attended several VTR meetings and worked on trying to get the VSCode debugger working
                for VTR. Experimented with the debugger on several smaller programs to figure this out
                and was successful at getting it to work for small programs. It seems that the VTR code
                is not being compiled with debug flags even though I set VTR to debug mode.
* **Friday**: Got debugging to work in VTR. It turns out I wasn't using the correct makefile. Attended 
              bootcamp meeting about fasm2bels and other open source FPGA github repositories. Implemented
              a fix in the regression test channel computation so that it only selects even numbers when
              unidirectional wires are used.

### Week 7: June 7, 2021

* **Monday**: Added a fix in the regression test channel computation so that bidirectional wires do
              not have their channel widths rounded to even numbers. Opened a feature request on the VTR
              github repo explaining what I had been working on. Also attended bootcamp meeting and ran
              a large number of tests to ensure that my changes did not impact other parts of the code.
* **Tuesday**: Finished ethics case study analysis and continued to experiment with VTR routing. Tested
               segments with channel widths approximating those found in Xilinx FPGAs and spent some time
               comparing 7 series FPGAs to look for patterns in the placement and routing.
* **Wednesday**: Attended immerse meetings and read through some of the symbiflow_arch_defs documentation.
                 Since the XML files are assembled using CMake I tried using their make commands to assemble
                 a complete XML architecture file but I have had no luck so far. Also continued to experiment
                 with modifications to an architecture file to determine other features we will need to add
                 to capture Xilinx 7 series FPGAs.
* **Thursday**: Successfully assembled an architecture file using the symbiflow_arch_defs tools. Attended
                VTR meeting and began working on trying to implement part of the symbiflow architecture into
                VTR. However, it seems that this will be a difficult process and that it will be hard to piece
                these parts together correctly in an architecture file.
* **Friday**: 