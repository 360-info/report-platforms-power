## Data in this report

[`species-survival.csv`](./species-survival.csv): fractions of surveyed websites that were still active at given points in time, grouped by the year they wer efirst active. Adapted from [McCarthy et al. 2020](doi.org/10.1371/journal.pone.0249993).

[`terms/`](./terms): Terms of Service, and secondary agreements, scaped from major tech platforms over time using [The Wayback Machine](http://waybackmachine.org). These include:
  * `[platform].csv`: statistics of the platform scrapes over time. Columns include:
    - `type`: `"primary"` if these are Terms of Service linked to on account creation; `"secondary"` if this is another agreement linked to by the primary agreement.
    - `policy_name`: The name of the policy.
    - `target_url`: The current URL of the policy, as requested of The Wayback Machine
    - `target_dt`: The date requested of The Wayback Machine
    - `snapshot_dt`: The URL of the policy snapshot given by The Wayback Machine
    - `snapshot_url`: The date of the snapshot returned by The Wayback Machine. This ought to be the closest snapshot to the date requested above.
    - `word_count`: The word count of the scraped policy.*
  * [`[platform]/[YY-MM-DD]/[policy].csv`]: the unnested tokens (words) of each scraped policy. Includes:
    - `para`: the paragraph number
    - `word`: the word

* Note: Spotify's Privacy Policy wasn't properly scraped in 2019, so `[terms/spotify.csv]` uses the word count of the _current_, live Privacy Policy in that year instead.
* 
