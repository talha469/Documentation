![App Screenshot](https://lh3.googleusercontent.com/Gzn87UteQMOjYLVJd5MzPtve0lVx2UZEfzuWUqQQXorj0rpZmwNA41sho_idBjx8n47mWwvQCReX-ZyN1fyUYw)

## Key Features

- **Multi-Language Support**: Supports Java, C#, JavaScript, Python, C++, PHP, and more.
- **Static Code Analysis**: Detects bugs, code smells, vulnerabilities, and security hotspots.
- **CI/CD Integration**: Integrates with Jenkins, GitLab CI, Bamboo, Azure DevOps, and other CI/CD tools.
- **Quality Gates**: Define conditions for code quality, such as code coverage, duplications, and critical issues.
- **Code Coverage**: Measures test coverage to show how much code is covered by unit tests.
- **Security Vulnerability Detection**: Identifies vulnerabilities based on OWASP Top 10 and SANS Top 25 standards.
- **Issue Tracking**: Tracks and provides detailed information on bugs, code smells, and vulnerabilities.

## Getting Started

For more detailed documentation and to get started with SonarQube, visit the official [SonarQube website](https://www.sonarqube.org/).

## License

SonarQube is available under the [GNU Lesser General Public License](https://www.gnu.org/licenses/lgpl-3.0.html).

## Installation

Sonar Qube can be downloaded from the website or docker images are also provided, In this tutorial
I am following Docker approach
*Note*: Please ensure docker daemon is up and running
opne cmd in **admin mode** and write the following
```sh
docker pull sonarqube
```

Postgres will be used as database and run the following command to pull its image

```sh
docker run -d --name sonarqube-db -e POSTGRES_USER=sonar -e POSTGRES_PASSWORD=sonar -e POSTGRES_DB=sonarqube postgres:alpine
```

ensure that psotgres container is running with the followign command on cmd
```bash
docker ps
```

Run SonarQube 
```bash
docker run -d --name sonarqube -p 9000:9000 --link sonarqube-db:db -e SONAR_JDBC_URL=jdbc:postgresql://db:5432/sonarqube -e SONAR_JDBC_USERNAME=sonar -e SONAR_JDBC_PASSWORD=sonar sonarqube
```

we have hosted the sonarqube on 9000 local port so type the following url in browser to access

```bash
http://localhost:9000/
```
username = admin
password = admin
![App Screenshot](https://github.com/talha469/Documentation/blob/main/Common/Media/SonarLogInScreen.png?raw=true)

update the password on next screen as required

Based on the preference, project can be choosend from a number of sources including Gitlab, Github etc
but for this demo, we are using a local project made with dot NET Core

Follow the instructions provided by sonarqube and run the command on cmd as guided by tool

```bash
dotnet tool install --global dotnet-sonarscanner
```

Run the following command in the root of the project
```bash
dotnet sonarscanner begin /k:"PWPAuxiliaryService" /d:sonar.host.url="http://localhost:9000"  /d:sonar.token=<your_token>
```

```bash
dotnet build
```

```bash
dotnet sonarscanner end /d:sonar.token=<your_token>
```

A detailed report will be shown on sonar UI opened in browser
![App Screenshot](https://github.com/talha469/Documentation/blob/main/Common/Media/sonarDetailedReport.png?raw=true)


## License

MIT