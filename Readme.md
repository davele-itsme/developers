# Mews developers

Information about development job opportunities and career at [Mews](https://mews.com). If you would like to know more about Mews, what we use, how we work etc, have a look at [About Mews](#about-mews) section. We also have a [Blog](https://developers.mews.com), [Twitter](https://twitter.com/MewsDevs) and [Facebook](https://www.facebook.com/MewsDevs/) with latest news about events, technical topics and life of devs at Mews.

Would you like to meet us? Hear us talk or check if we're coming to your area? Check out our [Eventbrite](https://www.eventbrite.com/o/mewsdevs-30252533666) for the events we organize. Recordings of our past talks can be found on our [YouTube](https://www.youtube.com/channel/UCrepPB-0Yryop41OuQbQR3w/playlists) channel.

**You can always reach us at [`tech.cm@mews.com`](mailto:tech.cm@mews.com).**

<a name='open-positions'/>

## 💼 Open positions

Currently, we are seeking highly experienced people for the following positions:
- [Mid/Senior Backend Developer - .NET C#](https://apply.workable.com/mews/j/094EDDB116/)
- [Senior Frontend Developer](https://apply.workable.com/mews/j/E8D97BFEB1/)
- [Senior Frontend Developer - Platform Team](https://apply.workable.com/mews/j/3FB93D9C0E/)
- [QA Automation Engineer](https://apply.workable.com/mews/j/55580F9394/)
- [QA Engineer](https://apply.workable.com/mews/j/15C60AF3DC/)
- [Mid/Senior Azure Data Engineer](https://apply.workable.com/mews/j/5975E7C0EB/)
- [Data Analyst](https://apply.workable.com/mews/j/5F83C23824/)
- [.NET Tooling Engineer](https://apply.workable.com/mews/j/0C135135A1/)
- [Azure Infrastructure Engineer](https://apply.workable.com/mews/j/2C839436E9/)
- [Working Student - Software developer talent, part-time](https://apply.workable.com/mews/j/9B62B88E63/)

For all openings, even outside tech, check our [open positions](https://www.mews.com/careers/jobs). If you don't match exactly any of the candidate profiles, but you feel you could contribute in some other way, let us know as well and we can figure it out.

<a name='about-mews'/>

## 📚 About Mews 

> We have revolutionised the way that hotels operate across all departments, through our mobile hotel management platform. We enable hoteliers to free themselves from boring administration (which we help automate) and rather focus on creating real customer experiences. Now live in 65+ countries in 2000+ hotels, we have truly started a revolution.

That's the marketing slogan. A more down-to-earth version of it would be, that we work on a system for hotel employees and their guests. The main goal is to improve the guest experience, by giving them possibility to have full control over their stay, possibility to check-in online, manage their profile, checkout and pay online, communicate with the reception etc. In consequence, that decreases workload on the hotel employees, because the guests actually do the work. The second big goal is opening up the system via APIs to 3rd party companies and developers, so that they can build interesting applications on top of our system. Or connect it with something else, which was traditionally very difficult in hospitality industry. If you'd like to know more, check this sample [sales-pitch](https://www.facebook.com/MewsSystems/videos/351045845603219/) which explains what we offer to our clients and which problems we solve.

In the following sections, we'll try to answer frequently asked question that we believe a candidate might have when considering application to Mews:

- [Product](#product) - what we build.
- [Technology](#technology) - how we build it.
- [Teamwork](#teamwork) - how do we cooperate.
- [Job](#job) - offices, working hours, salaries.
- [Students](#students) - part-time opportunities for students.
- [Relocation](#relocatoin) - for non Czech-based candidates.

<a name='product'/>

### 🏨 Product 

- **What are the applications you are building?** The biggest part is the system for employees of hotels (receptionists, housekeepers, accountants, revenue managers, essentially everybody). For them, we also have native mobile applications with a subset of the functionality. Then we have web applicaton for guests of the hotels and booking widget that hotels can put to their websites. We also offer hotels a kiosk application that they can put into their lobby and guests can checkin there. The full list of products is visible on our [website](https://www.mews.com/en/products).
- **What are your plans for the future?** We don't create fixed long term roadmaps. We plan and commit for the upcoming 4 months. And the rest of the roadmap represents rather a list of opportunities or problems we're going to solve most likely. You can check presentation of our CPO about [2021 roadmap](https://www.youtube.com/watch?v=Mr-FhBnouvg).
- **How do you handle if different hotels want different features?** We have some features that hotels can choose to enable or disable, according to their preferences. However, all of the various features are available to all hotels. Being SaaS, we have only one feature set and single live environment. We have successfully avoided doing any white-labeling or custom development and the bigger we are, the less likely this will ever happen.
- **Does your system have public APIs?** Yes and it's one of its strengths. We try to take it really seriously and make it as user-friendly as possible for other developers to integrate with us. We also have a dedicated team to help the integration partners and give them advices how to best connect to us. So now, we have over 500 companies consuming our APIs. You can find out more here: https://mews-systems.gitbook.io/connector-api/
- **Do you produce any open source code?** Yes, some of the things we have done are now open sourced, but as it takes a lot of time to maintain, we try to be very careful with what we decide to make open. We decided that we'll be open sourcing mainly fiscalization libraries (like EET), becuase it's annoying having to implement it when some government decides to introduce it. We're also pretty active in the Flutter space when it comes to opensourcing. You can check our public repositories here https://github.com/MewsSystems.

<a name='technology'/>

### 👨‍💻 Technology 

- **Which technologies do you use?** Generally, we try to use technology that is familiar to the development community. The benefit of using common technology is that everybody knows it well, and if not, they're able to Google the answers to their own questions. We also try to avoid building in-house solutions, but rather use third party services for responsibilities that are not directly related to our business (e.g. Rapid7 for logging, Sentry for error reporting, SendGrid for mailing). We want to focus on our product. Check our [Stackshare](https://stackshare.io/mews-systems/mews) to see a full list of what we use and check our [Platform documentation](https://www.mews.com/platform-documentation) for philosophy behind our platform and other things like security, disaster recovery, infrastructure etc.
- **What is architecture of the backend?** The "executable" is a plain ASP.NET MVC application with no extra caveats. We use Entity Framework code-first approach, and we use Azure DB (a version of MSSQL) as our database. We run the application in Azure using App Services, so we don't need to manage the web servers or virtual machines. We are currently in the process of migrationg to .NET 5 from .NET Framework 4.8 with the expected finish in the first half of 2021. In general, there is data layer to access Azure DB, Azure Storage, Cosmos DB and Redis, business layer consisting of various components and a transactional layer (web, API, background jobs). BTW you can check our [Awesome Mews](https://github.com/MewsSystems/awesome-mews) reading list to see what is our philosophy, not only on backend.
- **How is frontend structured?** We keep all our apps in one monorepo to share as much code as possible. All the apps are written on the same stack based on Redux, React and styled-components. We are migrating everything to TypeScript - current adoption is around one third of the codebase. We are fans of functional programming and apply many of its principles to our code. Some data-heavy screens like reports are rendered on server using Razor templates, but we've successfully eliminated all legacy technologies like jQuery or Angular. In order to have consistent visual style and share code, all our applications are using our design system https://mews.design/. 
- **How does technology stack for mobile apps look like?** Operator kiosk application is written from scratch in Kotlin. For Android development we use a standard set of libraries: Dagger, Retrofit, RxKotlin (and Detekt + ktlint for static code analysis). We have a fully set up CI/CD process for Operator app and are moving into this direction for other apps as well. iOS and Android versions of Mobile Commander were initially written in Swift and Java, but last year we've migrated them to Flutter.
- **Do you create microservices?** At the moment, no. The idea of having small units that are responsible for a specific task is great, however this architecture style would not match the current needs of our system. But with increasing size of the system and teams, we might evolve there naturally. However at the moment, we see modular monolith as the way for us going forward as our Head of Backend described in his [blogpost](https://developers.mews.com/are-we-migrating-to-microservices-and-should-you/).
- **What is your test coverage?** We do not know. We do not measure code coverage, primarily because we do not see it as a crucial parameter. We're trying to optimimze the value/effort when it comes to tests, so we've covered majority of the system with end-to-end UI tests, all APIs with integration tests and crucial libraries and components with unit tests and integration tests. We're also working on performance regression tests.
- **How often do you deploy?** The best answer would be daily. All our applications are delivered continuously which means that when a pull request gets merged, a new version of the application is released to development environment. Daily, we do deploy a snapshot of development environment to staging environment (feature-freeze) and the next day, from staging to production. Long-term, we're moving towards fully continuous delivery to production.

<a name='teamwork'/>

### ⛹️ Teamwork 

- **Do you look for any specialists?** Both, specialists and "generic" developers are fine. We try to learn about their individual skills over time. Once we know what they enjoy working on, we try to embrace that and assign projects that each person is interested in. We have enough of a workload for the generic developers, which extends to all layers of our applications including new features and/or fixing bugs. At the moment, we have 15 teams with different responsibilities, so there are options to choose from. As we grow, we start to look for specialists especially in platform teams (infrastructure, tooling, design systems).
- **Which team will I work in?** That's hard to tell in advance. Basically there are two factors that we take into account. First, we look at past experience and preferences of the candidate. Second, we look at our own needs that are based on company strategy. And combine those two inputs to find the best match in one of 15 teams in the following divisions and families (segmented by customers they build products for):
  - Product
    - B2B - Applications for hotels and their employees.
    - B2C - Applications for guests that visit the hotels.
    - Connectivity - APIs for 3rd party companies that integrate to us and provide services to hotels.
    - Payments - Online payment solutions used by B2B and B2C applications.
  - Platform
    - Backend - Infrastructure, libraries, tooling etc. used by backend developers in other teams.
    - Fronted - Design system, tools and shared libraries used by frontend developers in other teams.
    - Data - Data warehouse and infrastructure used by data analysts within the company.
- **How is your workload structured and prioritized?** We operate on 4-month periods (tertiles). For those periods, we plan product and technical initiatives with investment ratio 2:1. Simply put, for 2 features, we do 1 consolidation. Consolidations are usually issues that originate in tech team like performance improvements, refactoring, elimination of technical debt, migrating to newer technologies. Product initiatives are primarily prioritized by product managers and other stakeholders, technical initiatives by tech leads and other people from tech department. This applies to all teams, both platform and product teams. On lower level, teams operate in 2-week sprints where the tech lead, together with the team, distributes the individual tasks. We try to avoid affinity within team to single type of work, e.g. one developer only bugfixing, another only building features.
- **Which versioning system do you use?** We host our code on GitHub, therefore we use git.
- **What is your branching workflow?** On backend, it's very similar to [Gitflow](https://nvie.com/posts/a-successful-git-branching-model/). On web and mobile applications, we have only master branch and feature branches, but that's just Gitflow without some branches.
- **Do you do code reviews?** Yes, for everything. Code review is a crucial part of how we work. We consider this a great practice, which helps the whole team understand what is happening in the system. As a developer, you not only gather feedback on your code (which helps you to improve), but you're also able to spread your knowledge and experience to others. It's also great platform for newcomers and juniors to ask questions and learn. For code-reviews we use GitHub pull requests. Currently, each pull request is reviewed by at least two people, one being senior. Such a dilligence requires really optimized code review process, currently our average pull request merge time is around 35 hours.
- **Do you work with continuous integration?** Once you open a pull request, our CI server (Azure DevOps) picks it up automatically and runs checks against the changes. Unless all checks have passed, you will not be able to merge your pull request.
- **Do you have any code style rules?** We believe in naming things the right way rather than adding comments. We have our own set of code style rules (99% of .NET FW rules on backend, AirBnb on frontend) that are run during any build. If your code violates any of the rules, no one will be able to build the project. The goal is to have a uniform code style throughout the whole platform. We also create our own analyzers for common mistakes that appear during code-reviews.
- **How often do you schedule refactoring?** We do not schedule refactoring. We consider it to be an integral part of development work. When implementing a new feature, it is important to verify that all of the team code and architecture quality standards are applied. The fixes and features should all be done properly from the beginning. Refactoring is also being done as part of technical roadmap which happens continuously, parallel to product roadmap.
- **How do you handle changes in the architecture of the system?** We try to introduce changes gradually while extending the capabilities of our system. For bigger changes, both on backend and frontend, we currently have platform teams whose only responsibility is to improve the system architecture, develop libraries and tools for other teams that are more focused on product. So platform teams prepare everything necessary in advance, so that product teams can adopt it in the upcoming period as part of their technical roadmap.
- **How many meetings would I have in a day?** That's up to team to decide, in most teams there is a short daily standup meeting. Once in a sprint, there is a grooming and planning meeting of the team (some teams have those merged). On Friday, there is a 30 minute meeting of all people in tech department with latest updates which then continues with 30 minute company-wide call, finishing with 30 minute company-wide question time. Averaging this out, it's like an hour a day. 
- **What is the company language?** In Prague office, where development is located, around 50% of people are Czech and the rest is mix of many other nationalities. Therefore most of the meetings and communication is held in English.

<a name='job'/>

### 🏢 Job

- **What does the office look like?** The office is located at [I.P. Pavlova square, 1789/5](https://www.google.com/maps/place/n%C3%A1m%C4%9Bst%C3%AD+I.+P.+Pavlova+1789%2F5,+120+00+Nov%C3%A9+M%C4%9Bsto/@50.0752762,14.4298992,3a,75y,184.78h,101.94t/data=!3m6!1e1!3m4!1s73pkxL_pvma3Oge6NEn3QQ!2e0!7i13312!8i6656!4m5!3m4!1s0x470b948c0ea2c643:0x3f011e15da2b48b!8m2!3d50.0749916!4d14.4298445), which is great in terms of transport options (metro line C, A, many trams).
- **Do you pay out special bonuses?** No, we do not. We prefer to pay good salaries transparently and on a regular basis so that you always know what you can count on. You can read more on our approach in a [blogpost](https://developers.mews.com/manage-people-like-a-boss/) by our CTO.
- **Do you have stock option plan?** Yes, every employee is awarded certain number of depository receipt options (an equivalent of stock option in Netherland jurisdiction).
- **How many years would it take to reach a senior position?** We have a bit of a different understanding of what "senior developer" means. To us, a senior developer takes full responsibility for some part or component of the system and does not need anyone to help them with their tasks or to look over their shoulder. For this reason, we cannot guarantee that you will become a senior developer. It's up to you to determine how quickly you can become that skilled. Furthermore, if you consider yourself to be a senior developer already, it may happen that we will not agree. In our job posts for senior positions, you can find a list of topics. A senior developer should ideally have deeper knowledge with at least some of them. To get better understanding of our compentency model, have a look at how we built it [like an RPG game](https://developers.mews.com/how-to-build-career-framework-like-an-rpg/).
- **Is it possible that a new junior developer would earn a higher salary than me as a senior developer?** No. We try to avoid frustrations about money and keep an eye on the salary of each person individually; we believe it should correspond to their skill level. Therefore, if we desperately needed to hire a junior developer with a salary higher than yours, we would increase all the salaries in the company so that the levels are kept intact. We want to pay salaries that are competitive to the market as we don't want you to leave because of a better salary offer. We don't have open salaries, but try to structure them as if they were.
- **Can I have a home office?** Yes, with the current world situation we became fully remote company. Prior to COVID, home office was a thing of trust. We need to be able to trust that you are producing the same amount and quality of work as when working from the office. If you have a home office but do not respond for 2 hours on Slack, that's suspicious. Home office is not a day off. When taking home office, we expect that you do not need anyone to help you accomplish your tasks that day and that you will not need to interrupt too many people via any communication channel. Post-COVID, we expect most people to adopt hybrid model with a few days in the office focused more on communication and collaboration and a few days at home dedicated to focused uninterrupted work.
- **What are the working hours?** That really depends on you. Every person has a different rhythm to their life. As long as you accomplish what you have promised to accomplish, it's up to you. Most people are in the office between 11:00 and 17:00. Although there is a lot of flexibility, your working hours should intersect with this time period so that you have opportunities to meet with the team and consult them regarding your work.

<a name='students'/>

### 🎓 Students

- **Is it possible to work for Mews while studying?** Yes, we have many students in the team, especially from [MFF CUNI](https://www.mff.cuni.cz/en) and [CTU](https://www.cvut.cz/en). We treat students just like any other employees (part-time), which means they're working on real projects, in product teams with other developers and getting market salary.
- **Do you provide any support for students?** Because Mews development team was founded by a group of students that met in school and were still studying, we know what it means to both work and study. Therefore we're OK with you having a month break during exam periods, so that you can prepare for the exams. Students also have lot of time flexibility because of their school schedules. And since we have graduates from both of the aforementioned schools in our team, we can also help with the studying.
- **Can I do a bachelor or master thesis for Mews?** Definitely, we have many ideas that are appropriate either for bachelor or master theses. Just reach out to us and we can discuss the possibilities.

<a name='relocation'/>

### ✈️ Relocation

- **What is the cost of living in Prague?** You can find it and compare with other cities at https://www.numbeo.com/cost-of-living/in/Prague.
- **How long does it take to relocate?** Unfortunately, it takes a lot of time; usually around 6 months. First, we must submit the job posting announcing your position to the Czech Labour office, where it must be pending publicly for 30 days for potential employees. After that, the paperwork is processed, and both governments have 30-60 days to finish the procedure. Regrettably, these offices like to take their time and therefore, it is difficult to give an exact estimate about how long it takes from start to finish.
- **Do you offer relocation packages?** Yes, we will support you with the relocation both from the organizational and administrative perpsective, but also from the financial perspective.
