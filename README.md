# Introduction to Git and GitHub

**Speaker:** Blaine Mooers, PhD  
**Email:** blaine-mooers@ou.edu  
**Phone:** 405-271-8300  
**Institution:** Laboratory of Biomolecular Structure and Function, Department of Biochemistry & Physiology, University of Oklahoma Health Campus, Oklahoma City  
**Event:** Oklahoma Data Science Workshop  
**Date:** September 19, 2025

## Overview

This presentation introduces Git version control and GitHub hosting for researchers, scientists, and programmers. It covers fundamental concepts, practical applications, and demonstrates real-world workflows for collaborative coding and writing projects.

## Objectives

- Demystify Git and GitHub terminology and concepts
- Explain Git's and GitHub's roles in version control and collaborative coding/writing
- Demonstrate practical uses of Git and GitHub in research workflows
- Prepare workshop participants to contribute to the DSW GitHub organization

## Key Topics Covered

### Version Control Fundamentals
- **Motivation:** "You know you are brilliant, but maybe you would like to understand what you did two weeks from now." - Linus Torvalds
- Traditional file tracking vs. Git's snapshot approach
- Benefits for scientists, writers, and programmers

### Git vs. Other Version Control Systems
- **Popular alternatives:** SVN, Mercurial, Perforce, CVS, Bazaar
- **Git advantages:**
  - Free and open source
  - Distributed nature
  - High performance
  - Non-linear workflows with branching
  - Efficient merging
  - Extensive tool integration
  - Strong community support

### GitHub and Git Hosting Services
- **GitHub:** Most popular Git hosting platform
- **Alternatives:** GitLab, Codeberg, Bitbucket, SourceForge
- GitHub statistics: 268,651,144 public repositories (as of presentation date)

### Making Research FAIR
GitHub helps make research:
- ✓ **Findable**
- ✓ **Accessible**  
- ✓ **Reusable**
- **Interoperable** (requires additional consideration)

## Practical Git Commands

### Initial Repository Setup
```bash
echo "# ProjectName" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/username/repository.git
git push -u origin main
```

### Daily Workflow Commands
```bash
git add filename
git commit -m "commit message"
git push
```

### Custom Bash Function for Git Add-Commit (gac)
```bash
gac () {
    echo "Function to git add a file and then commit the changes with a message."
    echo "Takes the name of a file and the message in a string."
    echo "Must set up repository in advance of using this function."
    if [ $# -lt 2 ]
    then
        echo "$0: not enough arguments" >&2
        echo "Usage: gca filename 'message about the commit'"
        return 2
    elif [ $# -gt 2 ]
    then
        echo "$0: too many arguments" >&2
        echo "Usage: gct "
        echo "Note absence of file extension .tex"
        return 2
    fi
    git add "$1"
    git commit -m "$2" "$1"
}
```

## Integration with Overleaf

The presentation demonstrates Git integration with Overleaf for collaborative LaTeX writing:

1. **Overleaf Git Menu:** Access through project settings
2. **Authentication:** Requires Git authentication token
3. **Clone Command:** 
   ```bash
   git clone https://git@git.overleaf.com/project-id
   ```

## Personal Git Usage Examples

### Repository Types
- Code repositories for research projects
- Slideshow presentations (like this one)
- Writing projects synchronized with Overleaf  
- Link collections and databases
- Configuration files and scripts

### Workflow Integration
- **Emacs Integration:** Define projects with .git directories
- **Version Control:** Local tracking with remote backups
- **Collaboration:** Multi-author papers with branching/merging
- **Cross-Platform:** Push/pull between GitHub and Codeberg

## Resources and Training

### Hands-on Training
- **Software Carpentry Workshop:** Version Control using Git/GitHub
- **When:** October 3, 9 AM to 12:30 PM
- **Where:** LL 123 Classroom, Bizzell Memorial Library
- **Instructor:** Dr. Mark Laufersweiler (laufers@ou.edu)
- **Registration:** https://libcal.ou.edu/event/14914295

### Recommended Reading
- *Pro Git* by Scott Chacon and Ben Straub - https://git-scm.com/book/en/v2
- *Beginning Git and GitHub* by Mariot Tsitoara (Second Edition)

### Links
- **Oklahoma Data Science Workshop:** https://mediasite.ou.edu/Mediasite/Channel/odsw
- **Git Official Documentation:** https://git-scm.com/
- **GitHub:** https://github.com/
- **Git Repository Statistics:** https://gitcharts.com



For questions about contributing to the ODSW organization, contact the workshop organizers or refer to the training resources listed above.
