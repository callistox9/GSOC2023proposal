











            Metacall/distributable-linux


ORGANIZATION – Metacall
Google Summer Of Code 2023


About me 

  Contact Information

    • Name: Soumya Sourav Guha
    • Time Zone: IST (UTC+5:30)
    • Chat handle: @soumyasourav:matrix.org
    • Github id: callistox9
    • Email: codecallisto@gmail.com


Brief Bio

I am hooked to open-source software development, an ambitious outgrowth of my personal interest 
to contribute to open-source communities.I B.tech Computer Science Undergrad at Poornima University, Jaipur, India, with cloud-computing as my major. 

I am Vice-Captain of Poorniam Paathshala, NGO that focuses on education of underprivileged children. Instagram-https://www.instagram.com/poornima_paathshala/

Links to Pull Requests
      
    • (open) runtimeLinkAdded – While going through documentation Metacall/core, Go runtime package was not added. So I attached a link to it.

    •  (open)  Typo Corrected – In the Metacall/guix-gcc-example, there was a minor typo that this PR shall fix.
      
    • (open) Msg updated – In the install.sh file in Metacall/install , I updated an echo statement.

I hope the PRs shall be of some relevance.

The Project
 
The Metacall/distributable-linux is the most suited distribution for Metacall. However, the project has environment variable issues and as encountered by me, there are many guix shell errors aswell.

My main objective for this project shall be to address all the issues present in the project solving the env variable issues, build scripts finding env-vars, write tests for more languages like Go, TypeScript , Ruby, cli.

There are many more issues and additionals that must be added to the project. I have read about the open issues, also added to nonguix in gitlab. Four out of six tasks have been done. Hopefully, I should be able to check on all the dependency issues and also write tests for same.

I shall improve embedder support for existing languages as an additional outcome to this project.
I will work on the metacall open issue for the zig application embedder, and shall complete all the tasks as mentioned in the open issue.

However, there is another requirement in the project. To add new archtecture for Linux and tests for the same. I have been learning to write docker scripts and use docker. To use Docker multi-arch for this requirement would be benificial to me as to this project aswell.

Tasks are many to complete, and the project difficulty is somewhat hard for it uses many skills and tools for its development. I am ready to give my all and completely indulge myself into this project.
I am ready to work 30 hrs a week or even more if needed. My enthusiasm for learning new technologies, skills is alot. For the whole timeline of this project, I shall work the best to complete this project and stick to this org even after this project is over, cause that is what open-source is for.

Timeline

Community bonding (4-May—28-May)

During this period, I would mainly focus on studying and going deep into guix shell, gnu, makefile and all all the way into solving the issues. I am already familiar with the project but I have to spent time on NetCore.

I will constantly be in touch with the mentors and getting help wherever needed. By the end, 
my aim is to 
    • Getting familiar with Docker Multi-arch for adding new architecture
    • GNU/guix , locales and binaries.
    • Cmake and build.
    • Netcore and the dependency errors.

My focus would to get as much knowledge as I can to conclude the project.
 
Coding Period Begins

WEEK 1 -- WEEK 4 (29 MAY -- 28 JUNE)

The main focus during this timeline would be to write script to search env-variables other than the way described in the install.sh file. Issue #5
    • For this, i will write a config file at the root cli-directory.Then define all the required environment variables in this file.
    • Then in the Guix package defination, i will write commands to copy all the config file into 
      the bin directory. The write commands to set env-variables using the very same config file.
      In this way, i will add all the env variables.Atlast, i will build and install the package using guix and this way environment variables will be set in cli.

Moreover, to write tests for additional languages like Go, Ruby, and typescript as they are not very well defined.Make a stadard way to define env in guix shell for cli and fix the Ruby module.
Issue #14
    • The Ruby runtime used by Metacall cannot find the module.I will make sure by installing nakogiri and make sure it is available in the ruby runtime used by metacall.
    • Now, the path where the ruby runtime by Metacall is running and coping this path.
      Probable command to find path is – metacallcli scripts/mult.rb
    • This path will be added to the example file ‘mult.rb’ . Hopefully, this way, the issue will be solved.


During this period, I will also solve this issue#15. I will follow all the steps as commented and address to its solution through these these steps.

WEEK 5 – WEEK 8 (29 JUNE – 28 JULY)

The main focus during this period would to implement netcore and backtrace support.Issue #1
    • For this i will add necessary build steps to the deps.sh to download and build netcore. Then use PKG_CONFIG_PATH to make netcore libs available to metacall build process.Also create nuget package and build C# loader. For this I will write necessary steps to the build.sh script.

    • I will create test cases for C# loader using a testing framework such as Nunit.Add the necessary build steps to the ‘tests/build.sh’ script to the C# Loader test suit.

To implement backtrace support , 
    • Initially i will create a guix package defination for the backward cpp library. I will do this by a .scm file in the guix/packages and define necessary steps to build dependencies for the package. Then update the metacall.scm file to include a call to add_external_project for the backwardcpp library. Also ,I will update all necessary configs, run tests for the same.

I will address to the issue #13. However, gnu/store is defualt prefix used. But we can configure the installation prefix for Metacall/distributable-linux by modifying the cmake file.By finding the cmake_install_prefix variable, that specifies the installation prefix for the built files, we can modify it to a path that we choose.




WEEK 9 – WEEK 12 (29 JULY – 28 AUGUST)
 
During this period, the motive would be to complete the documentation of the project and to add support to new architecture as per a requirement for the project.
 
    • For this, I would use Docker multi-arch. I am current thinking of ‘arm64’ linux architecture.
    • I will update the Docker file and install required packages and dependencies and compile the project with appropriate flags.I will use docker multi arch to build and test the new architecture.

This is a complex task and as stated earlier, I am ready to devote myself into the project.Tools used will be docker , buildkit and scripting using bash.

GSOC PERIOD ENDS


Apart from mentioned schedule, i will be :-

    • Push my code in a regular basis so that my mentor shall keep track of whatever work I am doing.
    • Send PR as soon as code is ready and cleaned-up, preferably before each evaluation deadline.

Languages and packages used

                C#, CMAKE, SCHEME, BUILDKIT, GUIX, DOCKER, GUILE, C/C++

HOW I PROPOSE TO COMPLETE THE PROJECT

I am pretty confident that I will be able to complete this project as I have been playing around this project for sometime and researching and finding ways to address all the issues in this project and also my the errors that I have encountered. The chat community is always available and the possible mentors to my respective project is very welcoming.

I have good command on git and github and will be pushing my code on a regular basis so that mentors can evaluate my work whenever they have time.I have experience in open-source development aswell as I have contributed to college club projects.

I will spend alot of time writing test codes for my project and plan the GSOC journey before the coding period starts. This will avoid me from having any problems later.

Even after the GSOC coding period ends, I will be actively coding to METACALL and be available if anybody has questions regarding my work.

Benefits to the community

Metacall/distributable-linux is the best suited for Metacall/core. But I is not complete.By resolving the issues and proposed idea, the project will be complete and a stable version of Metacall Linux Distributable will be available.




GSOC

Have you ever participated in GSOC?
     
        No, this is my first time participating in GSOC.


Are you applying to other projects?
    
       No, I am only applying to Metacall Organization.

Commitments

From the beginnig of GSOC timeline, from community bonding to the end of coding period, I am commited to give 6-7 hours on the project. Even during the community bonding period, I am ready to give 6 hours everyday to understand code base and discuss with my mentors.

The project that I have chosen has Hard difficulty level. During the coding period, I am ready to give as much hours of work daily, even if it means 8 hours to write and complete the project. Even during the weekends, I will be commited to the project. 

Eligibility

I am currently enrolled in a 4-year B.tech Computer Science bachelor program(in Semester – 6).
I have not participated in GSOC before and I am 18 years and above. I am also allowed to receive payments from Google as per laws in my country.

I am persistent to commit myself into the development and completion of the project for as many hours it may take. So, yes I am eligible for this project and as well as for GSOC.




















