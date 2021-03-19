# Evaluating Media

When seeking out information about vaccine management systems, one popular place to look is news stories about system failures. These stories can be highly visible, and rightfully raise concern about problems that various jurisdictions have come across in using particular systems.

When doing so, however, it can be helpful to keep the following facts in mind:

* _Context_: What information is typically missing from these reports, and what questions should you ask to find it out?
* _Defining success_: How do you evaluate the "success" of a given system under consideration?
* _Clarifying difficulties_: How do you characterize difficulties that a given system has been experiencing?

## Understanding Context

Often, news stories are missing critical context. It is important to seek to understand, where possible, certain more specific facts in order to better understand what has happened and what can be done about it. In particular, ask:

<table>
  <thead>
    <tr>
      <th style="text-align:left">Question</th>
      <th style="text-align:left">Explanation</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <p></p>
        <p>What system is being used? Consult with us to find more information about
          which jurisdictions are using which systems, if it is unspecified.</p>
      </td>
      <td style="text-align:left">
        <p></p>
        <ol>
          <li>When you find other systems, check what other jurisdictions are using
            the same system, and whether they have come across similar issues.</li>
          <li>Keep in mind that different systems may be in use for different aspects
            of the scheduling process - check <a href="../tech-tools.md">tool categories</a> and
            <a
            href="../vendor-landscape/">vendor categories</a>for more information.</li>
        </ol>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p></p>
        <p>What specific problems are people encountering?</p>
      </td>
      <td style="text-align:left">
        <p></p>
        <p>Beware of catch-all terms like &quot;bugs&quot;. Instead, check section
          <a
          href="common-challenges.md">common challenges</a>to see if this challenge is unique to the system
            under discussion. Keep in mind that systems vary in their ability to address
            these challenges - please <a href="https://www.usdigitalresponse.org/request-help/">reach out</a> to
            ask for detailed vendor evaluations.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p></p>
        <p>Exactly how many people are impacted, and what populations do they represent?</p>
      </td>
      <td style="text-align:left">
        <p></p>
        <ol>
          <li>A small number of very passionate people can make a loud splash, but</li>
          <li>Even if there are only a small number of people impacted, especially if
            they represent underrepresented groups or those most in need of the vaccine
            their concerns should be taken very seriously.</li>
        </ol>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p></p>
        <p>If related to downtime, ask a few questions:</p>
      </td>
      <td style="text-align:left">
        <p></p>
        <ol>
          <li>How long was the system down?
            <ol>
              <li>Take particular note of outages lasting more than 10 minutes at a time</li>
              <li>Outages longer than this are unacceptable, and avoidable with modern best-practices
                in Site Reliability Engineering</li>
            </ol>
          </li>
          <li>Have there been multiple outages?
            <ol>
              <li>These should be infrequent, and decrease in frequency over time if they
                happen at all.</li>
            </ol>
          </li>
          <li>Was the root cause identified and rectified? Is there mention of a post
            mortem?
            <ol>
              <li>This kind of open discussion of system outages is expected in a modern
                software development environment.</li>
            </ol>
          </li>
        </ol>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p></p>
        <p>How did the vendor respond to these issues?</p>
      </td>
      <td style="text-align:left">
        <p></p>
        <ol>
          <li>Systems should be robust to high-traffic situations. If they are not,
            the system is at fault, not the audience using it.</li>
          <li>Be careful if the vendor pinpoints &quot;user error&quot; as a cause -
            these systems should work with a variety of audiences with a variety of
            backgrounds, and where necessary, should provide training in how to use
            them.</li>
        </ol>
      </td>
    </tr>
  </tbody>
</table>

## Defining Success

When a system is praised, particularly in news media, it is important to seek clarity on the following questions, to better understand the nature of this success:

<table>
  <thead>
    <tr>
      <th style="text-align:left">Question</th>
      <th style="text-align:left">Explanation</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <p></p>
        <p>Has the system been stress tested under real, significant load?</p>
      </td>
      <td style="text-align:left">
        <p></p>
        <p>Sometimes systems can declare victory too early, before real users have
          attempted to use them. See if you can find information on the exact number
          of providers and end-users currently using this system</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p></p>
        <p>How many providers have signed up with the tool?</p>
      </td>
      <td style="text-align:left">
        <p></p>
        <p>Difficulties in integrating with individual system EHRs and IISs becomes
          obvious at scale - pay close attention to how many jurisdictions, systems,
          and sites within jurisdictions that a given tool has integrated with</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p></p>
        <p>Who is writing the article or providing advice?</p>
      </td>
      <td style="text-align:left">
        <p></p>
        <p>Be aware of the source of a given article, it may have come from a PR
          firm or other entity with an interest in touting success and hiding other
          indicators.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p></p>
        <p>What brand names have been attached to the effort, and what is the true
          nature of their involvement?</p>
      </td>
      <td style="text-align:left">
        <ol>
          <li>A brand name in one field does not translate to a brand name in another</li>
          <li>This is a unique area with unique challenges - be aware of the nature
            of the company offering the solution, their history, and background</li>
        </ol>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">What are some tangible, numeric measures?</td>
      <td style="text-align:left">
        <p></p>
        <p>There are a number of factors at play in how &quot;successful&quot; a
          given jurisdiction has been at administering vaccines. Try to keep an eye
          on tangible, numeric measures where possible, such as: vaccination rate
          / 100K and percentage of vaccines administered vs. delivered.</p>
        <p></p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">What is correlated vs. caused?</td>
      <td style="text-align:left">
        <p></p>
        <p>Be aware that there are a number of factors that can make the determination
          of a &quot;successful&quot; system more complicated. Consider the below
          when establishing correlation vs. causation of certain numeric indicators:</p>
        <ol>
          <li>&quot;Centralization&quot; of health system (see CDC&apos;s <a href="https://www.cdc.gov/publichealthgateway/sitesgovernance/index.html">Governance Models</a>)</li>
          <li>Percentage of residents receiving vaccination through federally-sponsored
            sites (mass vaccination sites) and systems (VA, IHS)</li>
          <li>Percentage of rural vs. urban residents</li>
          <li>Political divisions concerning vaccine hesitancy</li>
          <li>Other demographic trends and numbers.</li>
        </ol>
      </td>
    </tr>
  </tbody>
</table>

## Clarifying difficulties

When you see bad news, consider the below caveats in assessing these difficulties:

<table>
  <thead>
    <tr>
      <th style="text-align:left">Call-out</th>
      <th style="text-align:left">Explanation</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <p></p>
        <p>Both the number of jurisdictions using a system, as well as the number
          that have switched off of a given system, are not necessarily indicative
          of the failures of that system</p>
      </td>
      <td style="text-align:left">
        <p></p>
        <ol>
          <li>News travels quickly, as do rumors. It can be difficult to conduct a rigorous
            root cause analysis on a particular problem, particularly when there is
            time pressure</li>
          <li>There is incentive to switch away from a given system as a means of making
            a statement. But there is often no guarantee that the system you switch <em>to</em> will
            not also have the same issues. Focus instead on the specific issues that
            lead to the system switch, and the specific ways the newer systems have
            addressed these issues.</li>
        </ol>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p></p>
        <p>A new system is not a cure-all</p>
      </td>
      <td style="text-align:left">
        <p></p>
        <p>It bears repeating: many problems will not be fixed by moving to a new
          scheduling system. Work with the vendor to see what can be done within
          the confines of your current system, and bring up the above as talking
          points as to the minimum required feature set of this solution. If the
          vendor is unable to offer these, it might make sense to look elsewhere.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p></p>
        <p>The ability of a system to improve is often more important than its initial
          mistakes</p>
      </td>
      <td style="text-align:left">
        <p></p>
        <p>Mistakes happen. But look for the trajectory of a given solution - does
          it have fewer issues over time? Is it adding features and fixing bugs to
          address user complaints, and are those features and bugs actually making
          a tangible difference?</p>
      </td>
    </tr>
  </tbody>
</table>



