# PA2588 DevSecOps: Playground for SAST (Static Application Security Testing)

This is part of the course DevSecOps.
You will cover two ways of including SAST in your development process.

## Preparation

  1. Click on [**Use this template**](https://github.com/new?template_name=pa2588-devsecops-sast&template_owner=bth-dipt-teaching)
     to create a new repository in your GitHub account (don't _fork_ it), and make sure to set the visibility to "Public".
  2. The GitHub actions should run automatically and be green.

## 1. Enable SAST in GitHub Actions

  3. In `.github/workflows/sast.yml`, uncomment the block labeled "Version 1" to enable Bandit.
     * After the next successful run of the GitHub actions, you should now see two security issues being reported.

## 2. Enable SAST locally

### Preparation

  4. Install (if you don't have it already) and open Visual Studio Code
  5. Install the "[pre-commit](https://marketplace.visualstudio.com/items?itemName=elagil.pre-commit-helper)" Extension, by Adrian Figueroa
  6. Clone your project into Visual Studio Code.

### Action

  7. Open a new terminal in Visual Studio, run `pre-commit install` to install the pre-commit hook
     * If `pre-commit` is not yet installed, run `brew install pre-commit` (if you have `brew` installed)
       or `pip3 install pre-commit` (otherwise)
  8. Add a comment line to `app.py`
  9. Run `git add app.py && git commit -m "Update app.py"` and see the commit fail with two security issues
