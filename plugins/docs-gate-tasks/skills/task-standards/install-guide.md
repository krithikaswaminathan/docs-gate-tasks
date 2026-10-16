# Installation guide checks

> **Sources** (paraphrased; which checks to include, their severities, and their scope are the
> author's own calls):
> - Pradeepa Somasundaram, ["How To Create a Software Installation Guide For Your Customer"](https://www.linkedin.com/pulse/how-create-software-installation-guide-your-customer-somasundaram/)
>   (February 2023).
> - The Good Docs Project, [installation guide template](https://www.thegooddocsproject.dev/template/installation-guide).
> - Diátaxis, ["The difference between a tutorial and how-to guide"](https://diataxis.fr/tutorials-how-to/)
>   (for how an installation guide differs from a tutorial).
>
> Anything still marked `TODO` is a placeholder. `review-task` treats a check that still says
> `TODO` as not defined and doesn't apply it.

## How to recognize an installation guide

An installation guide takes the reader from not having the product to having it installed and
working. It's written for a reader who is technically capable and has a job to do, not for someone
learning the product. It's kept separate from how-to guides, which assume the product is already
installed. It may be its own page or a section of a README.

Unlike a tutorial, an installation guide may branch — by operating system, version, or hosting
provider — and assumes the reader can handle surprises. Whether the material is basic or advanced
doesn't decide the type.

## Checks

### I1. Purpose and result

- **What to look for**: what's being installed, what it does, and what the reader will have when
  they're done.
- **Passes when**: near the start, the page says what the product is and what it's for, and what
  the installation produces.
- **Severity if it fails**: **Blocker**.
- **Doesn't apply when**: always applies.

### I2. Installation types, with help choosing

- **What to look for**: the variants of the installation — by operating system, product version,
  or hosting provider.
- **Passes when**: the page lists every variant it covers, for example in a table, and gives the
  reader enough to choose between them.
- **Severity if it fails**: **Nice-to-have**.
- **Doesn't apply when**: there's only one way to install the product.

### I3. System requirements

- **What to look for**: the hardware and software the installation needs — operating system
  versions, processor, memory, disk space, and so on.
- **Passes when**: the requirements are listed before the installation steps, for each
  installation type where they differ.
- **Severity if it fails**: **Blocker**.
- **Doesn't apply when**: always applies.

### I4. Prerequisites

- **What to look for**: what the reader must have or do before starting — dependencies and their
  required versions, accounts, permissions, or skills.
- **Passes when**: the page has a section before the steps (for example "Before you begin") that
  lists every prerequisite the steps rely on.
- **Severity if it fails**: **Blocker**.
- **Doesn't apply when**: always applies.

### I5. Numbered steps, each with its result

- **What to look for**: how the installation steps are laid out.
- **Passes when**: the steps are numbered, each starts with the action to take, and each is followed
  by what the reader should see when it worked.
- **Severity if it fails**: **Nice-to-have**.
- **Doesn't apply when**: always applies.

### I6. Recommends one path

- **What to look for**: where the reader has a choice between installation options.
- **Passes when**: the page says which option most readers should pick.
- **Severity if it fails**: **Nice-to-have**.
- **Doesn't apply when**: there's only one way to install the product.

### I7. Every method covered

- **What to look for**: the operating systems and installation methods the page says are supported.
- **Passes when**: each one has complete steps of its own, from start to a verified install. A
  method that's mentioned as supported but has no steps, or whose steps stop partway, fails.
- **Severity if it fails**: **Blocker**. In the report, name the methods without complete steps.
- **Doesn't apply when**: there's only one way to install the product.

### I8. Verify the installation

- **What to look for**: how the reader confirms the installation worked.
- **Passes when**: the page gives a command or check to run, and the output or result the reader
  should see.
- **Severity if it fails**: **Blocker**.
- **Doesn't apply when**: always applies.

### I9. Configuration

- **What to look for**: settings the reader should change or check after installing.
- **Passes when**: the page lists the settings to configure, with their expected or default values,
  or says plainly that no configuration is needed.
- **Severity if it fails**: **Blocker**.
- **Doesn't apply when**: always applies.

### I10. Upgrade and downgrade

- **What to look for**: how to move to a newer version, and back to an older one.
- **Passes when**: the page explains how to upgrade, and either how to roll back to an earlier
  version or that rolling back isn't supported.
- **Severity if it fails**: **Blocker**.
- **Doesn't apply when**: always applies.

### I11. Uninstall

- **What to look for**: how to remove the product.
- **Passes when**: the page explains how to uninstall the product cleanly, including anything it
  leaves behind (configuration files, data, services).
- **Severity if it fails**: **Nice-to-have**.
- **Doesn't apply when**: always applies.

### I12. Troubleshooting

- **What to look for**: problems the reader is likely to hit during installation.
- **Passes when**: the page lists common installation problems, with their causes and fixes, and
  says where to get help if those don't solve it.
- **Severity if it fails**: **Blocker**.
- **Doesn't apply when**: always applies.

### I13. Next steps

- **What to look for**: what the reader should do once the product is installed.
- **Passes when**: the page ends by pointing to what to do or read next, such as a getting-started
  tutorial.
- **Severity if it fails**: **Blocker**.
- **Doesn't apply when**: always applies.

### I14. License

- **What to look for**: the terms the software is used and distributed under.
- **Passes when**: the page states the license, or links to it or to the terms of use.
- **Severity if it fails**: **Nice-to-have**.
- **Doesn't apply when**: always applies.

### I15. Version stated

- **What to look for**: the product version the guide covers.
- **Passes when**: the page names the exact version, or range of versions, the instructions apply
  to.
- **Severity if it fails**: **Nice-to-have**.
- **Doesn't apply when**: always applies.
