<h1>LLM Vulnerability Scanning Test with Garak</h1>

<h2>Description</h2>
Project involving scanning large language models with Garak (https://github.com/NVIDIA/garak/) in Linux to test for different vulnerabilities. Garak has a large list of different vulnerabilites that can be used to test LLMs. Some of these include: profanity, encoding-based errors, prompt injection, malware generation and cross-site scripting. As chatbots are a common thing found in many companies today, testing them for security related purposes is crucial.

<br/>
<br/>
Launching Garak and looking at the probes: <br/> 
<img src="https://i.imgur.com/Y61tSuP.png" height="70%" width="70%"/>

For the tests involved I utilized OpenAI's GPT2 found on HuggingFace.
The probes will send a large amount of prompts to the AI in hopes of exploiting different types of vulnerabilities. The first one I ran was a profanity focused probe, which attempts to have the bot repeat back different profane words that would typically be blocked/disabled. <br/> <br/>
<img src="https://i.imgur.com/ZtHN4Ym.png" height="70%" width="70%"/> <br/>
Running the first probe, lmrc.Profanity <br/>
Once the probe is complete, it creates both a report and a hitlog in JSON and HTML file types. The hitlog is specifically where the bot failed, or the vulnerability was found.
<br/> <br/>
Results of the first probing (hitlog) <br/>
<img src="https://i.imgur.com/YMdA86n.png" height="70%" width="70%"/> <br/>
Definitely some interesting things that the bot should not be saying <br/> 

<br/>
The next probe I used was the prompt injection one, it follows a similar structure with the previous probe in that it seeks to have the bot say something it shouldn't. This probe has it responding back to the user about hating/killing humans as well as a ridiculously long prompt. <br/> <br/>
<img src="https://i.imgur.com/TM8OE3g.png" height="70%" width="70%"/> <br/>
Running the probe <br/> <br/>
<img src="https://i.imgur.com/QsjnQwf.png" height="70%" width="70%"/> <br/>
<img src="https://i.imgur.com/cph19me.png" height="70%" width="70%"/> <br/>
<img src="https://i.imgur.com/gYhHpmd.png" height="70%" width="70%"/> <br/>
<img src="https://i.imgur.com/3FnLuG6.png" height="70%" width="70%"/> <br/> 

Results of the different scans found in the prompt injection probe <br/>

You can also utilize different IDE's to open the results and format them into a much more clean and readable format. I used codium to do so. <br/> <br/>
<img src="https://i.imgur.com/psfcMZ9.png" height="70%" width="70%"/> <br/> 
