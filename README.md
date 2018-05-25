# pch-chart
"
TL;DR: just fill my chart with ducks!

Make a GitHub repo pch-chart.

Run in local shell:
mkdir pch-chart
cd pch-chart
curl -o pattern-ducks.txt https://raw.githubusercontent.com/stcruy/public-contrib-hack/master/pattern-ducks.txt
curl -o patternToDates.js https://raw.githubusercontent.com/stcruy/public-contrib-hack/master/patternToDates.js
curl -o datesToCommits.sh https://raw.githubusercontent.com/stcruy/public-contrib-hack/master/datesToCommits.sh
chmod +x datesToCommits.sh

git init
git remote add origin git@github.com:<YOUR_USERNAME_HERE>/pch-chart.git
node patternToDates.js pattern-ducks.txt
./datesToCommits.sh
git push -u origin master

To queue a duck that will slide in view during the upcoming weeks, add:
curl -o pattern-duck.txt https://raw.githubusercontent.com/stcruy/public-contrib-hack/master/pattern-duck.txt
node patternToDates.js pattern-duck.txt "<FIRST_SUNDAY_AFTER_MOST_RECENT_SATURDAY_HERE__example:>15 Mar 2015"
./datesToCommits.sh
git push -u origin master

"
