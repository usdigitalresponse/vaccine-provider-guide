# Common Challenges

Vaccine scheduling systems frequently encounter many of the same issues. Look below for information about what these issues are 

<table>
  <thead>
    <tr>
      <th style="text-align:left">Challenge</th>
      <th style="text-align:left">Explanation</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <p></p>
        <p>System outages / Scalability</p>
      </td>
      <td style="text-align:left">
        <p></p>
        <p>See our section on <a href="outages-and-downtime.md">outages and downtime</a> for
          more information</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p></p>
        <p>User Interface issues</p>
      </td>
      <td style="text-align:left">
        <p></p>
        <p>We have seen a number of trends in user interface design of these systems.
          More on this in our section on <a href="common-user-interface-issues.md">common user interface issues</a>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p></p>
        <p>Translations or accessibility issues</p>
      </td>
      <td style="text-align:left">
        <p></p>
        <p>These should be a high priority given the audiences these tools need to
          be able to work with. They are also easier to fix, if they are prioritized.
          But keep in mind:</p>
        <ol>
          <li>Google Translate is often not an acceptable translation mechanism - when
            translating short words and phrases, Google lacks the context to differentiate
            between such words as &quot;back&quot; as in &quot;a person&apos;s back&quot;,
            and &quot;back&quot; as in &quot;previous page&quot;.</li>
          <li>Prefer human-created translations to ensure preservation of context</li>
          <li>Evaluate both the original text and translated text with an eye toward
            readability/literacy level. Many text editors have functionality built
            in to assess this.</li>
        </ol>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p></p>
        <p>Overbooking/double booking</p>
      </td>
      <td style="text-align:left">
        <p>This is likely related to one of the following, which can be harder to
          fix:</p>
        <p>1. The lack of an appointment hold mechanism - certain systems have this,
          others do not. Adding this to a system that does not have it can be difficult.</p>
        <p>2. Fallout from the system being down or being under heavy traffic</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Local Differences</td>
      <td style="text-align:left">
        <p></p>
        <p>EHR and IIS systems present a challenge on the ground and differ widely
          between jurisdictions. Just because a system is easy to implement in one
          place does not make it easy to implement in another.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p></p>
        <p>User lockout / account issues</p>
      </td>
      <td style="text-align:left">
        <p></p>
        <p>These can be caused by:</p>
        <ol>
          <li>The way login is implemented in a particular system
            <ol>
              <li>Where possible, and see our user interface guidelines for more information,
                a system should avoid asking for too much information up front - balance
                freeing a user from having to enter new information with the need to fill
                out a long list of questions.</li>
            </ol>
          </li>
          <li>Fallout from the system being down or being under heavy traffic
            <ol>
              <li>Ensure that the system under investigation fails gracefully when there
                is downtime or diminished capacity.</li>
            </ol>
          </li>
        </ol>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Unauthorized Access</td>
      <td style="text-align:left">There are ways to make links single-use, which certain services have implemented,
        but many have not. This is a medium-difficulty ask, though depends on the
        system. The benefits of this are significant, in that they save people
        time when they would otherwise show up for an appointment they are not
        eligible for.</td>
    </tr>
  </tbody>
</table>

