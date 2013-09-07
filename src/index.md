
# A Real Database Rethink

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

<h2 data-bespoke-bullet>Databases: a short history</h2>

<p data-bespoke-bullet>
***1960s***: From tapes and batch to disks, shared access and interactivity
</p>

<p data-bespoke-bullet>
***Late 1960s***: Navigational databases: *links*
</p>

<p data-bespoke-bullet>
***Early 1970s***: The relational model: *content*
</p>

<p data-bespoke-bullet>
***Late 1970s***: SQL
</p>

<p data-bespoke-bullet>
***Early 1980s***: A database on my desktop (dBASE and its ilk)
</p>

<p data-bespoke-bullet>
***Late 1980s***: Object Orient ALL THE THINGS!
</p>

<p data-bespoke-bullet>
***2000s***: Speed and scale: NoSQL
<br><span data-bespoke-bullet>
*"NewSQL": never let a beautiful abstraction go to waste*
</span>
</p>

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

## The tyranny of a beautiful abstraction

An abstraction that fits many problems very well is tempting to use in solving more problems

e.g. relational databases, relational algebra and SQL

The problem should rule the solution, not the reverse.

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

## So what is a Database?

**A tool for interacting with structured data, externalised from the core of our application**

 * Persistence
 * Performance
 * Simplify access to complex data

And sometimes...

 * Shared access
 * Scalability

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

## The Node approach

<div data-bespoke-bullet>

<ul>
 <li>Small core, vibrant user-land</li>
 <li>Extreme modularity</li>
 <li>Reimplement everything in JavaScript!</li>
</ul>

</div>
<div data-bespoke-bullet>

<p>Applied to databases?</p>

<ul>
 <li>Small core: LevelUP</li>
 <li>Everything as a module</li>
 <li>Pulling in many aspects of database *practice* &amp; *theory*</li>
</ul>

<p>
(internal data relationships, data relationship with the application, storage technology, distributed methodologies)
</p>

</div>

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

<table class="ecosystem">
  <tr class="tools">
    <td class="section"><span>Tools</span></td>
    <td><table><tr>
      <td>lev</td>
      <td>levelweb</td>
      <td></td>
      <td></td>
      <td></td>
    </tr></table></td>
  </tr>
  <tr class="packages">
    <td class="section"><span>Packages</span></td>
    <td><table><tr>
      <td>tacodb</td>
      <td>couchup</td>
      <td>LevelGraph</td>
      <td>firedup</td>
      <td>level-assoc</td>
      <td></td>
      <td></td>
      <td></td>
    </tr><tr>
      <td>level-static</td>
      <td>level-store</td>
      <td>level-session</td>
      <td>level-fs</td>
      <td>LevelTTLCache</td>
      <td></td>
      <td></td>
      <td></td>
    </tr></table></td>
  </tr>
  <tr class="extensions">
    <td class="section"><span>Extensions</span></td>
    <td><table><tr>
      <td>level-live-stream</td>
      <td>map-reduce</td>
      <td>level-queryengine</td>
      <td>Level-Multiply</td>
      <td></td>
      <td></td>
      <td></td>
    </tr><tr>
      <td>multilevel</td>
      <td>level-replicate</td>
      <td>level-master</td>
      <td>Level TTL</td>
      <td></td>
      <td></td>
      <td></td>
    </tr></table></td>
  </tr>
  <tr class="pluggability">
    <td class="section"><span>Pluggability</span></td>
    <td><table><tr>
      <td>sublevel</td>
      <td>level-hooks</td>
      <td>level-mutex</td>
      <td></td>
      <td></td>
      <td></td>
    </tr></table></td>
  </tr>
  <tr class="core">
    <td class="section"><span>Core</span></td>
    <td colspan="10">
      <table><tr><td>
        LevelUP
      </td></tr></table>
    </td>
  </tr>
  <tr class="storage">
    <td class="section"><span>Storage</span></td>
    <td colspan="10"><table><tr>
      <td class="rotate"><span><b>LevelDOWN</b></span></td>
      <td class="rotate"><span>LevelDOWN (Hyper)</span></td>
      <td class="rotate"><span>LevelDOWN (Basho)</span></td>
      <td class="rotate"><span>MemDOWN</span></td>
      <td class="rotate"><span>level.js</span></td>
      <td class="rotate"><span>leveldown-gap</span></td>
      <td class="rotate"><span>LMDB</span></td>
      <td class="rotate"><span>mysqlDOWN</span></td>
    </tr></table>
    </td>
  </tr>
</table>

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

## LevelUP

Backed by a key/value store for arbitrary data, lexicographically sorted by key

 * Core operations: `put()`, `get()`, `del()`
 * Batch writes
 * ReadStream *the secret sauce*
 * WriteStream *for convenience*

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

## ReadStream

The core query mechanism to access sorted data

Arbitrary *start* and *end*
