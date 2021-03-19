# Outages and Downtime

Vaccine scheduling systems must be available when people need them. To enable this, we recommend these systems adopt the [best practices](https://sre.google/sre-book/table-of-contents/) of Site-Reliability Engineering, which we will detail below, with mind to specific issues we have come across in evaluating various jurisdiction solutions.

Ways to use these recommendations:

* For jurisdictions seeking new systems, the below concerns, in conjunction with the rest of this guide, should be part of the initial considerations around which system to acquire and/or switch to
* For jurisdictions who have an ongoing relationship with a particular provider, the below can be part of the recommendations and requests that the jurisdiction can make of their existing provider

SRE best practices means that these services should maintain high service availability; engage in demand forecasting and capacity planning in order to respond gracefully to surges in traffic; adopt robust change management; allow for seamless system upgrades with minimal to no downtime; and they should log, track, and seek to minimize Mean Time To Repair.

One important framing for all of these recommendations is the so-called "Service Reliability Hierarchy", summarized in the Google [SRE Book](https://sre.google/sre-book/part-III-practices/). With this model in mind, we organize our recommendations along this pyramid, going from the most basic, \(likely easiest to make\) changes \(which correspond to the base\), to the most advanced, and perhaps most difficult to implement \(corresponding to the peak\).

Below is the list of prioritized concerns to investigate, discuss, and where relevant, address:

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
        <p>Are logging, monitoring, and alerting built in?</p>
      </td>
      <td style="text-align:left">
        <p></p>
        <p>These should be standard features of these systems to ensure early problem
          detection:</p>
        <ol>
          <li>Logs to catch issues as they happen</li>
          <li>Monitoring to see whether the site is down or under heavy load</li>
          <li>Alerting to let the on-call person know right when there is an outage</li>
        </ol>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Does the site have a plan in place for when there is downtime?</td>
      <td
      style="text-align:left">
        <p></p>
        <p>In the unlikely event of downtime, these systems should:</p>
        <ul>
          <li>Gracefully failover to a minimal site</li>
          <li>Gracefully disable non-functioning features</li>
          <li>Ensure data integrity and avoid data corruption</li>
        </ul>
        </td>
    </tr>
    <tr>
      <td style="text-align:left">Are there formalized uptime guarantees?</td>
      <td style="text-align:left">
        <p></p>
        <p>Is there a guarantee built into the contract of system uptime percentage?
          Such Service Level Agreement (SLA) clauses are standard in many agreements,
          and a good idea, especially if coupled with explicit callouts of Service-Level
          Indicators (SLIs) to watch for, working toward explicit Service-Level Objectives
          (SLOs) in formally defining this uptime. This should also be accompanied
          by a guaranteed Mean Time to Repair, on-call procedure, and support.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p></p>
        <p>Has the vendor planned for the possibility of downtime?</p>
      </td>
      <td style="text-align:left">
        <p></p>
        <ol>
          <li>Vendors should engage in capacity planning and forecasting, with a mind
            to the unique traffic scenarios that this website represents.</li>
          <li>Systems should come equipped with an incident response plan, complete
            with Incident Management Process and dedicated on-call rotation</li>
          <li>During development, developers of these systems should adopt distributed
            load testing tools to simulate realistic high-traffic scenarios. Systems
            should not be rushed to the finish line without such robust testing infrastructure
            in place.</li>
        </ol>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p></p>
        <p>Is it easy to update the system?</p>
      </td>
      <td style="text-align:left">
        <p></p>
        <ol>
          <li>Can the system be updated without downtime? It should not be necessary
            to take a website down entirely to perform upgrades if it is using modern
            best-practice development techniques.</li>
          <li>Vendors should adopt best practices of release engineering, including
            continuous build and deployment and configuration management in order to
            release new versions easily and seamlessly.</li>
        </ol>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p></p>
        <p>Is it robust to intentional attacks / bots?</p>
      </td>
      <td style="text-align:left">
        <p></p>
        <p>In addition to dealing with high standard load, these systems should implement
          DoS / DDoS Protection, by means of IP blocking, DDoS protection, and other
          similar tools, to avoid such malicious actors.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Is the system cloud-based?</td>
      <td style="text-align:left">
        <p></p>
        <ol>
          <li>A scalable, cloud-native solution is preferred, to be able to handle frequent
            traffic surges through failover, load-balancing, and other strategies.</li>
          <li>Note that just being cloud-based is often not sufficient in and of itself
            - the tool should adopt proper capacity planning and use cloud resources
            in a way that allows for rapid and frequent traffic surges: it should utilize
            multiple geographic availability zones, load balancers, and other modern
            practices to ensure that the impact of a surge in traffic is limited.</li>
        </ol>
      </td>
    </tr>
  </tbody>
</table>



