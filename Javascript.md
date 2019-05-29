## Javascript


### Best Practices
nasw5 javascript tips and tidbits





## Angular
### Promises
Batman and Promises.

### Performance
Angular takes too long to compile / serve / compile tests - increase node process memory.

Using Node for GitHub Actions Workflow Automation — How to write Github Actions using Node instead of shell scripts.  search for.
NLP.js: Natural Language Utilities for Node.js — Guess the language of a text, stemming/tokenization, sentiment analysis, etc.
AXA  search for.
source map false on flakey tests
npm run ng test --source-map=false
https://stackoverflow.com/questions/50761206/how-do-i-turn-off-source-maps-for-angular-6-ng-test
https://stackoverflow.com/questions/45722256/how-do-i-debug-a-object-errorevent-thrown-error-in-my-karma-jasmine-tests/46840229#46840229
npx webdriver-manager update --versions.chrome=2.37
then instead of npm run e2e, use:
npm run ng e2e --webdriver-update=false
kill all chrome processes if cannot start debugger in VS code
TASKKILL /IM chrome.exe /F
console.log(Object.values(object1));            
console.log(JSON.stringify(result))
< https://stackoverflow.com/questions/11616630/json-stringify-avoid-typeerror-converting-circular-structure-to-json and https://makandracards.com/makandra/28847-dealing-with-typeerror-converting-circular-structure-to-json-on-javascript
npm run compodoc
https://www.intertech.com/Blog/protractor-testing-10-tips-and-tricks/
https://medium.com/google-developer-experts/angular-2-testing-guide-a485b6cb1ef0
https://medium.com/@me_37286/yoni-goldberg-javascript-nodejs-testing-best-practices-2b98924c9347 <-- really good article.
https://medium.com/@bencabanes/angular-component-testing-with-examples-7c52b2b7035e
Fuzzy matching: https://github.com/aceakash/string-similarity
In local branch:
-           running e2e cross browser – needs wd start first (in local), then:
o          ACTUALLY: protractor protractor.conf.js --grep=@smoke    note no quotes.
@addyosmani: Tip: Get the unique values of an array in JavaScript. https://twitter.com/addyosmani/status/1080727964411674624/photo/1
Shared via TweetCaster
