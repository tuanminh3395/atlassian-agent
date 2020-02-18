# Atlassian Agent

#### Support (almost any version, include 8.0):
* JIRA Software [FAQ] (doc / JIRA_FAQ.md)
* JIRA Core
* JIRA Service Desk
* JIRA plugin: Capture
* JIRA plugin: Training
* JIRA plugin: Portfolio
* Confluence [Special Note for Windows] (doc / Confluence_FAQ.md)
* Confluence plugin: Questions
* Confluence plugin: Team Calendars
* Bamboo [FAQ] (doc / Bamboo_FAQ.md)
* Bitbucket [FAQ] (doc / Bitbucket_FAQ.md)
* FishEye [FAQ] (doc / FishEye_Crucible_FAQ.md)
* Crowd [FAQ] (doc / Crowd_FAQ.md)
* Crucible [FAQ] (doc / FishEye_Crucible_FAQ.md)
* Third party plugins

## Instructions for use

### Advantage
* Supports almost all Atlassian products, as well as plugins (including third-party plugins in the plugin market).
* Support DataCenter mode.
* Compared to traditional crack, you can easily upgrade your service without re-cracking it again.
* Provides java based command line keygen, which is more convenient to use in terminal environment.
* Open source project, you know what you did when you cracked it.

### Download
* Download the [release] (https://github.com/pengzhile/atlassian-agent/releases) package of this project directly.

### Compile by yourself
* Clone the source code of this project, compile after executing `mvn package` in the same directory of pom.xml.
* Use `atlassian-agent-jar-with-dependencies.jar` produced by` target` directory instead of `atlassian-agent.jar`!
* * If you don't know what I'm talking about, it's better to download my compiled package directly. *

### Using help
* Cracking requires a complete set of use. You can't just crack plugins. You must first use `atlassian-agent.jar` to crack the service.
* If you have obtained `atlassian-agent.jar`, you can try to execute` java -jar atlassian-agent.jar` and see the output help.
* The help here is based on the Atflusian Confluence service.

### Configure Agent
1. Place `atlassian-agent.jar` in a location that you will not delete randomly (all Atlassian services on your server can share the same` atlassian-agent.jar`).
2. Set the environment variable `JAVA_OPTS` (this is actually an environment variable for Java, which is used to specify the parameters attached when it starts the java program) and attach the` -javaagent` parameter. You can do this:
   * You can put: `export JAVA_OPTS ="-javaagent: /path/to/atlassian-agent.jar $ {JAVA_OPTS} "` into a file like `.bashrc` or` .bash_profile`.
   * You can put: `export JAVA_OPTS ="-javaagent: /path/to/atlassian-agent.jar $ {JAVA_OPTS} "` into the `setenv.sh` or` bin directory` where the service is installed setenv.bat (for windows) `.
   * You can also execute it directly from the command line: `JAVA_OPTS ="-javaagent: /path/to/atlassian-agent.jar "/ path / to / start-confluence.sh` to start your service.
   * Or other methods you know to modify environment variables, but if you have unrelated services on your machine, it is not recommended to modify the global `JAVA_OPTS` environment variable.
   * In short, you can find a way to attach the `-javaagent` parameter to the java process to be started.
3. After configuration, please restart your Confluence service.
4. If you want to verify that the configuration is successful, you can do this:
   * Execute a similar command: `ps aux | grep java` Find the corresponding process and see if the` -javaagent` parameter is correctly attached.
   * Similar to the software installation directory: `/ path / to / confluence / logs / catalina.out` The Tomcat log should be found:` ========= agent working ========= ` Output text.

### Using KeyGen
* You have to make sure the agent has been configured, please refer to the instructions above.
* When you try to execute `java -jar / path / to / atlassian-agent.jar`, you should see the output of KeyGen parameter help.
* Please take a closer look at the role of each parameter, especially the value range of the `-p` parameter.
* The third-party plugin takes its `application key / plugin keyword` as the` -p` parameter. For example: `-p com.gliffy.integration.confluence`
* During the installation of the Atlassian service you should see a server id similar to: AAAA-BBBB-CCCC-DDDD
* Provide correct parameters. Running KeyGen will output the calculated activation code in the terminal.
* Copy the generated activation code to activate the service you want to use.
* Give a chestnut: `java -jar atlassian-agent.jar -p conf -m aaa@bbb.com -n my_name -o https://zhile.io -s ABCD-1234-EFGH-5678`

### Declaration
* This project is only used for personal study and research, not for commercial use!
* For commercial use, please purchase genuine copy from [Atlassian] (https://www.atlassian.com), thank you for your cooperation!
* This project uses the `GNU General Public License v3.0` open source license!
* It is not allowed to say that my code is badly written, for me `PHP` is the best language in the world (not convinced).

### communicate with
* Post an issue to this project.
* You are welcome to improve this project together, please send PR.
* You can join QQ group: 30347511 to communicate with me in real time.
* Visit the website: [https://zhile.io] (https://zhile.io) Leave me a message.

### Enthusiastic netizen tutorial (thanks to the original author, invasion and deletion!)
* [confluence installation and crack] (https://www.qinjj.tech/2019/01/04/confluence%20install/)
* [[Black Technology] Atlassian Product Line Full Crack] (https://tech.cuixiangbin.com/?p=1248)
* [Install JIRA and Confluence via Docker (cracked version)] (https://www.jianshu.com/p/b95ceabd3e9d)
* [Install JIRA and Confluence via Docker (cracked version)] (https://my.oschina.net/wuweixiang/blog/3014644)
