# MBitcoinCash.ProjectSetup

This repository is used to configure project setup that applies to all sub-projects in the MBitcoinCash family.

### NuGet pacakges

Following NuGet pacakges are installed whit this package:
* Microsoft.CodeAnalyzis.FxCopAnalyzers (2.6.1) - used to run various code quality and correctnes analyzers. 
* StyleCop.Analyzers (1.1.0-beta004) - used to enforce code style rules.

### stylecop.json

This file is used to configure following StyleCop rules:

* Company name
* Copyright text at the begining of each source file
* Required documentation for all private and public interfaces, elements and fields

### CodeAnalysisRuleSet.ruleset

This file is used to configure FxCop rulesets that should be applied. All rules are set to Error level to enforce maximum correctnes from the start.
Specific rules can be excluded later on as needed base if consencus between developers is reached.

### AssemblyInfo.cs

This file is used to fix FxCop rule CA1014 which requires to mark all assemblies CLS complient.

### MBitcoinCash.ProjectSetup.props

This file is used to include all previously described files into project and configure some of the default project settings:
* Adds linked folder ProjectSetupConfig
* Adds stylecop.json as linked file to ProjectSetupConfig
* Adds AssemblyInfo.cs as linked file to ProjectSetupConfig
* Adds CodeAnalysisRuleSet.ruleset as linked file to ProjectSetupConfig
* Configures all warnings as errors