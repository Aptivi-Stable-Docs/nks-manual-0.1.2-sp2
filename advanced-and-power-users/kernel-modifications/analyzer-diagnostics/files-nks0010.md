---
description: Use Listing.CreateList()
icon: chart-mixed
---

# Files - NKS0010

This analyzer provides the following strings:

<table><thead><tr><th width="174">Context</th><th>String</th></tr></thead><tbody><tr><td>Error List</td><td>Caller uses <code>Directory.GetFileSystemEntries</code> instead of <code>FilesystemTools.CreateList()</code></td></tr><tr><td>Suggestion Box</td><td>Use <code>FilesystemTools.CreateList()</code> instead of <code>Directory.GetFileSystemEntries</code></td></tr><tr><td>Description</td><td><code>FilesystemTools.CreateList()</code> returns a list of <code>FileSystemEntry</code> instances that provides you information about a file, as well as a wrapper to the <code>FileSystemInfo</code> instance for that file.</td></tr></tbody></table>

### Extended Description

This code analyzer detects the usage of `GetFileSystemEntries` from the standard `Directory` class found in the `System.IO` namespace.

The `GetFileSystemEntries()` from the `Directory` class gives you a randomly-sorted list of files and directories, which may not be convenient for TUI applications, such as the interactive TUI.

`CreateList()` takes care of that by sorting directories and files in an alphabetical order by putting the directories first before the files. This way, this listing can then be used for interactive applications.

### Analysis Comparison

To get a brief insight about how this analyzer works, compare the two code blocks shown to you below:

#### Before the fix

<pre class="language-csharp" data-title="Somewhere in your mod code..." data-line-numbers><code class="lang-csharp">public static void MyFunction()
{
<strong>    var files = Directory.GetFileSystemEntries(PathsManagement.AppDataPath);
</strong>}
</code></pre>

#### After the fix

<pre class="language-csharp" data-title="Somewhere in your mod code..." data-line-numbers><code class="lang-csharp">public static void MyFunction()
{
<strong>    var files = FilesystemTools.CreateList(PathsManagement.AppDataPath);
</strong>}
</code></pre>

### Suppression

You can suppress this suggestion by including it in the appropriate place, whichever is convenient.

For more information about how to suppress any warning issued by the Nitrocid analyzer, visit the below page:

{% embed url="https://learn.microsoft.com/en-us/dotnet/fundamentals/code-analysis/suppress-warnings" %}

### Recommendation

We recommend that every caller which use this function use the recommended abovementioned method.
