# Project 3 Starter - IGME-340

This is your repo for Project 3. Your code for the Prototype App and the Final App goes here instead of in a zip. Everything about the project itself (requirements, what's graded, the documentation and video) is in the spec: [Project 3: Roll-Your-Own Flutter App](https://github.com/jptweb/IGME-340-Shared/blob/main/projects/p3_roll_your_own_instructions.md).

It starts as a plain Flutter app with a title bar and one line of text. `shared_preferences` is already in `pubspec.yaml`, since Project 3 requires it. You've almost certainly started your project somewhere else already, so Section II is the part to read.

---

## I. Get the Code

**Work in your own repo, not the template.** Accepting the assignment creates a private repo just for you, named `igme-340-project-3-<your-github-username>`. Don't fork `IGME-340/project3_starter` or click "Use this template" on it. I can't see work pushed anywhere else, so it won't count.

Clone it the same way as the participation repos and the Project 2 repo, with GitHub Desktop or `git clone <your-repo-url>`. Step by step: [Participation Repos](https://github.com/jptweb/IGME-340-Shared/blob/main/documents/participation.md).

**Don't clone into a path with spaces.** `Documents/IGME 340/` will cause failures later that have nothing to do with your code. Use something like `Documents/igme-340/`.

---

## II. Already Started? Bring Your Whole Project In

Most of you have a project going already. Move all of it into this repo. Don't copy just `lib/`: your app icon, splash screen, and app name live in the `android/` and `ios/` folders, and you'd lose them.

1. In your cloned repo folder, delete everything you can see (`lib`, `android`, `pubspec.yaml`, all of it). The hidden `.git` folder has to stay. It's what makes this folder your repo. If you can't see a `.git` folder, good, leave it that way.
2. Open your existing project folder and copy everything in it into the repo folder, **except** `build/` and `.dart_tool/`. If your old project has its own hidden `.git` folder, don't copy that either.
3. Open the repo folder in VS Code. It should be the folder that contains `pubspec.yaml`, not the one above it.
4. Run `flutter pub get`, then run the app and make sure it still works.
5. Commit with a message like "Bring in my project so far" and push.

That first commit can be the whole project at once. That's fine. From there on, commit as you go (Section IV).

After the push, look at your repo on github.com. You should see `lib`, `pubspec.yaml`, and your platform folders, and you should **not** see a `build` folder. If you do, your project is missing its `.gitignore`: copy the one from [the starter](https://github.com/IGME-340/project3_starter/blob/main/.gitignore) into your repo folder and Slack me.

Starting fresh instead? Skip all of that and build right here.

---

## III. Run It

```bash
flutter pub get
flutter run
```

I grade on the Android emulator (or the iOS Simulator if that's what you target), so run it there regularly, not just at the end. Chrome is fine for quick checks, but plenty of packages behave differently in a browser.

---

## IV. Commit and Push As You Go

Push whenever something works: a new screen, the save and load, a game mechanic, a bug fixed. Small commits with real messages ("Add settings page", "Fix crash when the list is empty") are what I'm hoping to see.

Your commit history is how I see your project come together. A whole project that arrives in one commit the night it's due is hard to tell apart from code that came from somewhere else, and that's when I'll ask you to walk me through it. It's also graded: the Final App needs at least 5 commits of your own, or it loses up to 10 points. The Prototype App has no minimum. One push of what you have so far is enough.

**One repo for both deliverables, graded by what's pushed at each due time.** For the Prototype App, that's whatever is in this repo at the prototype deadline. Then keep working here: for the Final App, it's whatever is here at the final deadline. Work that's only on your laptop doesn't count. Each of those dropboxes in MyCourses takes your repo link instead of a file. The Documentation and Video dropboxes haven't changed.

**API keys can stay in.** This repo is private, and I need the key to run your app.

### How to push

**GitHub Desktop:** write a summary, click **Commit to main**, then **Push origin**.

**Command line:**

```bash
git add .
git commit -m "Add settings page"
git push
```

---

## V. If Something Goes Wrong

| Problem | What to do |
|---|---|
| The app won't run after you copied your project in | Make sure VS Code has the folder that contains `pubspec.yaml` open, then run `flutter clean` and `flutter pub get`. |
| The push is huge or takes forever | A `build` folder probably got committed. Check that your repo folder has a `.gitignore` file (see Section II), then Slack me and I'll help you back it out. |
| "Unable to load asset" | Check that your `assets/` folder made it over and that `pubspec.yaml` still lists it. Stop the app and run it again (hot reload doesn't pick up new assets). |
| GitHub Desktop says the folder isn't a repository | The hidden `.git` folder got deleted. Clone your repo again into a new folder and redo Section II. |
| `git push` asks for a password | GitHub wants a token, not your account password. Easiest fix is to install [GitHub CLI](https://cli.github.com) and run `gh auth login`. |
| `flutter pub get` complains about SDK versions | Run `flutter --version` and send me the output on Slack. |
| Something else | Slack me. Don't sit on it quietly, a broken environment compounds fast. |
