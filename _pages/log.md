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
* **Friday**: Ran regression tests to compare modified versions of VTR architectures to their originals, 
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
* **Friday**: Tried to assemble a VTR architecture file with a Xilinx slicel site, but it is taking a long time
              as I predicted. Each piece of the file has had to be copied in recursively from the symbiflow
              arch defs repo and I have been making modicifcations according to the error messages that I am
              getting from VTR. In addition, I have been unable to complete the packing stage of VPR as it 
              appears to be expecting .latch primitives despite the symbiflow files using custom flip flops.

### Week 8: June 14, 2021

* **Monday**: Worked on getting the slicel to place and route in VTR and I was ulimately successful. We 
              discovered that in order for the slicel to work we needed an eblif file or to simplify the
              slicel flip flops to match the .latch primitive in the blif file output by ODIN II. I accomplished
              this by removing everything on the flip flops except the D, Q, and clk ports. Also cleaned up my 
              code and merged in changes from the main VTR branch.
* **Tuesday**: Got the CLBLL_L, CLBLL_R, CLBLM_R, and CLBLM_R to place and route successfully in VTR. Each one
               picks slicels instead of slicems, but that could be due to the verilog file input and we might not
               need slicems anyways. Started to look through the symbiflow architecture file to see if they
               implemented any of the Xilinx inerconnects.
* **Wednesday**: Studied the Xilinx interconnects in Vivado and determined that the symbiflow files only contain
                 information about the CLB sites and their primitives. It is hard to tell if the local wires that
                 run through the interconnects to the switchboxes use any global routing resources, but it
                 doesn't appear that they do. Also attended immerse meetings.
* **Thursday**: Attened weekly VTR meeting and re-read parts of the netcracker paper to find info on the local
                site routing in Xilinx CLBs. However, I'm not sure where to begin on attempting to implement 
                this in VTR. Also checked and ran tests on my channel width code because I think I might want to
                open a pull request for it. Fixed a bug in my txt_to_csv.py script and helped Jonathan with some
                git things.
* **Friday**: Made some small fixes to my VTR branch so it would pass more of the checks on github. Examined the
              switch boxes and interconnects in Vivado and created a file documenting what I found. Experimented
              with some of the QoR settings since just one file failed the strong QoR check, but I couldn't figure
              out what was causing it to be different.

### Week 9: June 21, 2021

* **Monday**: Cleaned up my channel width code, tested it, created a new branch, and opened a draft pull request
              for it. Nearly finished implementing the fixes suggested by Vaughn Betz and it now passes all checks.
              Also attended FPGA bootcamp meeting about Vivado IP block designs and using Vitis to program a board.
* **Tuesday**: Finished implementing the fixes on the channel width code and updated my pull request. It should be
               accepted soon after it is reviewed one last time. Also worked on cleaning up my VTR files and continued
               looking for ways to implement interconnects in VTR in addition to other features we might need.
* **Wednesday**: Attended immerse meetings and FPGA bootcamp meeting about Vitis HLS. Reviewed VTR architecture
                 reference about wire connections and studied these connections in one of the example architectures.
* **Thursday**: Attended VTR meetings and discussed the channel width code that I submitted a pull request for. Ran
                tests on existing architectures with differing channel widths to see if they are scaling properly.
                It seems that they are not quite scaling properly, so the rr_graph code will likely need to be changed. 
                Documented pin fan in/out percentages to determine how inaccurate the scaling is.
* **Friday**: Finished documenting the pin fan in/out and began to search through the rr_graph code to figure out how
              it works. Determined that the get_seg_track algorithm in rr_graph and rr_graph2 needs to be modified so
              that it creates one set for the x direction and one set for the y direction rather than one set for the
              entire FPGA. Fortunately the t_chan_width struct already stores info about the channel width x max and 
              the channel width y max.

### Week 10: June 28, 2021

* **Monday**: Continued to study and modify the rr_graph code. It turns out that it is going to be a lot more work than
              I originally thought and I am not sure what most of these functions do or how they work. However, I made
              some progress and was able to get a high level understanding of how the rr_graph is built.
* **Tuesday**: Went through most of the build_rr_graph function to understand how it works. Made some modifications
               to the rr_graph code and began to split it up into x and y segments. Also resolved errors that I began
               to encounter as I started to change the code.
* **Wednesday**: Helped with chip camp cleanroom module and briefly looked over some code in rr_graph2.cpp.
* **Thursday**: Continued to experiment with the rr_graph code and understand it fully. Attended VTR meeting and
                started to add some documentation to functions without any. Also started working on modifying the
                alloc_and_load_actual_fc function so that it applies the correct fc value to channels of different
                widths.
* **Friday**: Made additional modifications to the alloc_and_load_actual_fc function, but it turns out that pins can be
              assigned randomly around a logic block. As a result, I will need to modify the function parameters so that
              the function has information about what part of the logic block the pin is located on. Also spent some time
              trying to determine the fc values of the pips for 7 series logic blocks.

### Week 11: July 5, 2021

* **Monday**: Independence Day Holiday.
* **Tuesday**: Continued to study the rr_graph code and make changes to it. It seems that the code that determines which
               side of the logic block a pin is located on comes after the code that assigns connections to each pin so
               I will have to find a way to get that information earlier. Also experimented with git and discarded some
               changes I had made to my VTR repo so that I can observe the original behavior again.
* **Wednesday**: Added additional documentation to several functions in the rr_graph code to better understand how
                 they work. Continued to observe the behavior of pin assignments and I am still unsure how they are
                 assigned to a specific side of a logic block. It seems that I will need to understand the code thoroughly
                 before I can begin to make any changes since I likely need to make large modifications to many of the
                 functions.
* **Thursday**: Attened VTR meetings and gave an update on what I have been working on. Began to put portions of the
                function that determines pin location in its own helper function to see if I can use existing code to
                get the location information earlier for the alloc_and_load_actual_fc function. I also experimented with
                other changes and began studying other functions that use the pin location information. 
* **Friday**: Began to implement the pin location information and determine if the connection counts are now correct.
              I am not sure how the io block determines pin location, since it has the same pin listed on all sides 
              in the location description. Hopefully this doesn't interfere with the connection alogrithm that I am
              creating or I will likely have to create a custom case for io blocks.

### Week 12: July 12, 2021

* **Monday**: Home in California on vacation.
* **Tuesday**: Home in California on vacation.
* **Wednesday**: Home in California on vacation.
* **Thursday**: Home in California on vacation.
* **Friday**: Home in California on vacation.

### Week 13: July 19, 2021

* **Monday**: Successfully modified the Fc value array for all logic blocks except for io blocks. Tested my changes and
              was able to successfully run VPR. However, my changes had an effect on designs with channels of equal widths,
              so I modified the alloc_and_load_actual_fc function to only use the new code for designs with channels of
              different widths. In addition, I am not sure if I need to now modify other parts of the rr_graph now that the
              fc values are correct and there are no regression tests that cover this since it is a new feature.
* **Tuesday**: Worked a half-day due to an optometrist appointment. Spent some time studying the rr_graph code to see if I
               could find how pin location works for io blocks, and discovered that it assigns the same pin to all sides.
               As a result, I am not sure how I can modify the io blocks so that they will work with the new code I created.
               Also began to look at other parts of the design in the GUI to see if there are other parts that are incorrect
               with different channel widths in the horizontal and vertical directions.
* **Wednesday**: 
* **Thursday**: 
* **Friday**: 