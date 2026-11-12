# Study rule set

`Study.list` contains 6,527 public domain rules for an adult-content routing category. It has no proxy endpoints, authentication parameters, or policy names.

## Sources and attribution

- [MetaCubeX/meta-rules-dat](https://github.com/MetaCubeX/meta-rules-dat), commit `458e716abd80ff8c6aee2b7d15c4f94b20e9d279`, [geo/geosite/category-porn.list](https://github.com/MetaCubeX/meta-rules-dat/blob/458e716abd80ff8c6aee2b7d15c4f94b20e9d279/geo/geosite/category-porn.list): 6,521 entries, GPL-3.0. The GPL text is included at [licenses/Study-GPL-3.0.txt](licenses/Study-GPL-3.0.txt). MetaCubeX identifies [V2Fly/domain-list-community](https://github.com/v2fly/domain-list-community) as an upstream source.
- [ACL4SSR/ACL4SSR](https://github.com/ACL4SSR/ACL4SSR), commit `9810a20772c143c04b0647521c9cce5dea3ac2f6`, [Clash/Ruleset/Porn.list](https://github.com/ACL4SSR/ACL4SSR/blob/9810a20772c143c04b0647521c9cce5dea3ac2f6/Clash/Ruleset/Porn.list): the two additional suffix rules `ahcdn.com` and `dditscdn.com`, [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/). All other old suffix rules are already covered by the MetaCubeX source. The broad `porn` keyword rule was not copied.

## Conversion

The five exact-domain entries remain `DOMAIN`; the 6,516 MetaCubeX entries beginning with `+.` become `DOMAIN-SUFFIX`. Adding the two legacy suffixes yielded 5 exact-domain and 6,518 suffix rules. The user-directed migration below adds four suffix rules, bringing the current total to 6,527 (5 exact-domain and 6,522 suffix rules). This conversion adds no keyword, regular-expression, script, or IP rules. The initial external file preserved the previous embedded snapshot with the client policy removed; the four subsequent user-directed supplements are appended below that original ordered snapshot.

## Use

Reference this file through Shadowrocket's `RULE-SET` and choose a policy or policy group in the main configuration. Category membership does not dictate blocking or proxying; the main configuration controls the action. Existing earlier exceptions continue to take precedence.

This is a manually maintained snapshot dated 2026-11-12. Client-side rule-set refreshes retrieve the latest file committed to this repository; no upstream synchronization or scheduled task is installed.

## User-directed supplements (2026-11-12)

At the user's explicit correction identifying four remaining inline video rules in a screenshot, these existing `DOMAIN-SUFFIX` rules were moved from the client's video category into `Study.list`: `91cg1.com`, `911dsj.com`, `bench.kckdpiqpp.com`, and `and.ikhjevmq.cc`. Their suffix-matching semantics are unchanged. These four entries are user-directed supplements from the existing configuration, not attributed to MetaCubeX or ACL4SSR. The main configuration now routes them through its existing Study RULE-SET policy.
