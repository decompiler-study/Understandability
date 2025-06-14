# Understandability

## Survey

***A. Setup For User Survey***

  The setup of our user survey for RQ1 is as follows.
1) *Survey Participants:* Our target participants include developers of Java decompilers, developers of popular Java open-source projects and academic researchers. Developers of decompilers possess specialized knowledge and experience in decompilation techniques, providing valuable insights into tool development and usage. Engaging with developers of open-source projects allows us to capture the perspectives of potential end users of Java decompilers in real-world software development scenarios. In detail, 234 developers from 8 well-known Java decompiler projects on GitHub, 451 developers from 10 popular Java projects, and 120 researchers majored in computer science from 3 world-famous universities have been selected as our target participants. Eventually, 805 developers and researchers were invited to participate in this user survey in total.
2) *Survey Platform:* E-mails, which were sourced from publicly accessible websites, have been employed to gather questionnaire responses from participants across different regions and backgrounds, during which anonymity is ensured.
3) *Survey Questions:* A total of 11 questions have been designed in the questionnaire. The first question (Q1) examines whether participants have prior experience with decompilers, while the remaining questions are categorized into three distinct groups: (1) the participants’ self-evaluation, including their education level (Q2), their experience in Java programming (Q3); experience in Java decompilers usage, including the Java decompilers ever used (Q4), the purpose they used the decompilers for (Q5) and the frequency of using decompilers (Q6); (2) the importance of Java decompilation (Q7), decompilation correctness (Q8), and decompilation understandability in the participants' view (Q9); (3) the frequency of decompilation failures (Q10) and understandability issues (Q11) encountered by participants.

<div style="text-align: center;">
  <figure>
	  <figcaption style="text-align: center;"><strong>Table I: Survey Questions. </strong><span id="fig:survey_questions"></span></figcaption>
    <img src="./figures/survey_questions.png" alt="Survey bar 1"  style="width: 100%; display: block; margin: 0 auto;">
  </figure>
</div>

  To note, we focus not only on the decompilation understandability but also on the decompilation correctness in the design of this survey, as correctness is another important concern in decompilation. It can help us have a better comprehension of the importance of decompilation understandability and frequency of understandability issues in comparison. Particularly, question Q1 is designed to help us exclude invalid responses from users who have never used Java decompilers. Questions Q7-Q11 are 10-point Likert scale questions with 10 selections ranging from 1 (not important/very rare) to 10 (very important/very frequent).

<div style="text-align: center;">
  <figure>
    <img src="./figures/survey_bar1.png" alt="Survey bar 1" style="width: 100%; display: block; margin: 0 auto;">
    <figcaption style="text-align: center;">(a) Respondents' self-evaluation and Java decompiler experience. <span id="fig:survey1"></span></figcaption>
  </figure>

  <figure>
    <img src="./figures/survey_bar2.png" alt="Survey bar 2" style="width: 100%; display: block; margin: 0 auto;">
    <figcaption style="text-align: center;">(b) Respondents' evaluation on the correctness and understandability of Java decompilation. <span id="fig:survey2"></span></figcaption>
  </figure>

  <figure>
    <img src="./figures/response_letter/importance_by_category.png" alt="Importance by category" style="width: 100%; display: block; margin: 0 auto;">
    <figcaption style="text-align: center;"><span>(c) Respondents' evaluation on the importance of correctness and understandability in terms of their education levels and roles.</span> <span id="fig:survey3"></span></figcaption>
  </figure>

  <p><strong>Figure 1: Survey results.</strong></p>
</div>

***B. Survey Results***

  Eventually, we received 33 valid survey responses, out of which 15 were from developers of Java decompilers, 9 were from developers of other Java projects, and 9 were from university researchers. Figure 1a presents the respondents' self-evaluation and their usage experience with Java decompilers. Among all 33 respondents, 97% (32 out of 33) hold at least a bachelor degree, with over half holding a master's degree or a PhD degree. In addition, 82% respondents (27 of 33) have more than five years of experience in Java programming. These facts indicate that the survey sample consists of respondents with advanced degrees and rich experience in Java programming. These respondents are likely to have a deeper understanding of Java programming and be encountered with a wider diversity of coding styles and practices. Hence, these respondents are better equipped to evaluate the correctness and the understandability of Java code, especially the decompiled code, making their responses more reliable.

  FernFlower, JD-GUI, Jadx and CFR,  are four of the most frequently used decompilers, and over 88% of respondents have used any one of the four decompilers. The purposes for using Java decompilers are quite diverse: the three most common motivations are bug detection (16 respondents), code reuse (9 respondents), and malware detection (9 respondents). Additionally, several other uses were reported, including privacy leakage detection (3 respondents), source code viewing (3 respondents), study (2 respondents), library logic understanding (1 respondent), and tool refinement (1 respondent). Regarding the usage experience of Java decompilers, 76% respondents use decompilers no less frequently than monthly, suggesting that most respondents are well-acquainted with Java decompilers, which in turn implies that their evaluations of these Java decompilers are likely to be relatively objective. 

  Figure 1b further illustrates the distribution of respondents' evaluation on the correctness and understandability of Java decompilation, in which 24% of respondents think that Java decompilation is extremely important (score 10), with an average score of 7.7. In detail, 97% of respondents assigned a score over 5 to the importance of decompilation correctness, while the corresponding figure for the importance of decompilation understandability is 94%. Their average scores are 8.5 and 8.3, respectively. Although 6% (2 out of 33) of respondents rated the importance of decompilation understandability below 5.5 (the midpoint), 33% (11 out of 33) considered it very important (score 10), a proportion even higher than that for decompilation correctness. These statistics suggest that developers and researchers in the wild regard decompilation understandability as important as its correctness.

  Similar trends have also been observed in the frequency of decompilation failures and understandability issues encountered by respondents. The average scores for the frequency of encountered decompilation failures and decompilation understandability issues are 4.8 and 5.7, indicating that understandability issues are more commonly encountered in daily Java decompiler usage. A detailed investigation reveals polarized opinions on the frequency of understandability issues: though 30% respondents (10 out of 33) rated the frequency of understandability issues as low (score 4 or lower), 52% regraded them as frequent (score 7 or higher), and 24% assigned a high score of 8, the most frequently-selected score among all options. 

  In addition, an interesting finding can be found in the importance of correctness of decompilation and understandability of decompiled code in terms of the education level and identity of the respondents. As depicted in Figure 1c, respondents with a master's degree or lower tend to prioritize correctness slightly more than understandability, whereas PhD holders place marginally greater importance on understandability over correctness. In terms of the roles of respondents, developers of Java decompilers  exhibit a slight preference for correctness over understandability, while developers of other Java projects view correctness and understandability as nearly equally important. In contrast, researchers tend to prioritize understandability, albeit marginally, over correctness. These findings suggest that for researchers, as well as those highly educated, attach more slight importance to decompilation understandability than correctness. Nevertheless, almost all respondents across various kinds of education levels and roles consistently regard both decompilation understandability and correctness as important attributes.

  While decompilation correctness has been widely studied, the understandability of decompilation, especially Java decompilation, remains unexplored. Our work aims to fill this gap by conducting the first comprehensive study on Java decompilation understandability. We investigate the typical causes of understandability issues, explore the potential for developing metrics to effectively assess understandability, and pave the way for future research in this area.

**CONCLUSION:** Java program developers and researchers in the wild regard the understandability of Java decompilation as important as its correctness, and decompilation understandability issues are even more commonly encountered than decompilation failures.
