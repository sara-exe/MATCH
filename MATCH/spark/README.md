Local Instructions
-

1. Make sure to change the sql credentials in MatchJDBC to match your own.

2. Right click on the MatchApp class in Maven and select run.

3. After building and running, go to https://localhost:8080/

Server Instructions
-
Password: cuece366match

1. create jar: `mvn clean package`
2. ssh into the server: `ssh -p5122 cooper@199.98.27.118`
3. kill current java processes: `killall -9 java`
4. exit: `exit`
5. navigate to local /target folder
6. scp jar to server: `scp -P5122 MATCH-services-1.0-SNAPSHOT.jar cooper@199.98.27.118:~`
7. ssh into server `ssh -p5122 cooper@199.98.27.118`
8. run as background process `nohup java -jar MATCH-services-1.0-SNAPSHOT.jar &`
9. exit: `exit`
10. Go to https://199.98.27.118:8080/ in browser and click through any warnings

Testing
-

1. Since you haven't logged in, it should redirect you to the sign in page.

2. Click login and try using bad or blank credentials. It should display a warning to user.

3. Try logging in as a test user. e.g. "test1", pass: "sarahuang" This will take you back to the root directory, but now that you have a valid cookie the server will recognize you're signed in and redirect to your list of friends. (Sara Huang has two)

4. Try clicking on the friends profiles, and on Sara's own profile

5. Try uploading an image.

6. Log out, the cookie will be removed from the server's list and it will no longer recognize you, so it should redirect you to the sign in page again.

7. Click register and try:
a) leaving fields blank 
b) using an already existing username (e.g. test1)
c) entering a non-number in max distance
d) not clicking 'Get Location' 
e) clicking 'Get Location'

8. Make a new account and log in with it.

