# stoops-hot-or-not

Tap-to-open Hot or Not slideshows, hosted on GitHub Pages.

- House, for Nate and Jami: https://natestoops-web.github.io/stoops-hot-or-not/
- Kids rooms: https://natestoops-web.github.io/stoops-hot-or-not/kids/
- Kids rooms, parents' GO / NO-GO screen: https://natestoops-web.github.io/stoops-hot-or-not/kids/?parents

Each page is a self-contained HTML file. Open the link in Safari and the first photo should appear.

## Kids GO / NO-GO filter

Nate (N) and Jami (J) each mark every kids idea GO or NO-GO at `kids/?parents`. Marks save on each phone. "Share / Load" sends a link (`kids/?parents#g=HON-GNG:...`) or a code to the other parent, and the newer mark wins.

The kids see an idea only if both parents marked it GO. Any NO-GO hides it, and an idea stays hidden until both have marked it.

The Summary tab's "Send kids' link" makes `kids/?ok=a1.<time>.<bitmask>`. Opening it on the kids' iPad or phone saves that filter there. With no filter, the kids page shows "Mom and Dad are still picking".

To lock in a default for every device, commit `kids/approved.json`:

    {"f":"stoops-kids-approved","v":1,"at":<unix seconds>,"ok":["K1","K2"]}

Whichever is newer, a saved link or approved.json (by `at`), wins.
