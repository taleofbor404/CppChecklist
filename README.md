# CppChecklist
A small checklist for a normal day's code review.

<h3>Tests</h3>
<ul>
<li>Create tests as early as possible.</li>
<li>Run existing tests as early as possible.</li>
</ul>

<h3>Includes</h3>
<ul>
<li>Proper include guard is added.</li>
<li>No duplicate includes.</li>
<li>Forward declare in hpp files as much as possible.</li>
<li>Proper include format: 
<ul>
<li>No relative/absolute paths.</li>
<li><> for library and system includes.</li>
<li>"" for user-defined type includes.</li>
</ul>
</li>
<li>Check proper include order.</li>
</ul>

<h3>Classes</h3>
<ul>
</li>
<li>Use initializer list for user-defined types for better performance.</li>
<li>Check proper const-ness of functions/parameters/members.</li>
<li>Check proper access modifiers (eg. move to private if not supposed to be accessed externally).</li>
<li>Private default constructors for static classes.</li>
</ul>

<h3>Parameters/Variables/Pointers</h3>
<ul>
<li>Use pass-by-reference as necessary (especially for large structs).</li>
<li>Check data types of values being passed in function parameters (eg. uint32_t being passed to a uint16_t parameter).</li>
<li>No hardcoded numbers.</li>
<li>Check that variables are initialized.</li>
<li>Check that pointers are initialized.</li>
<li>Check proper use of smart pointers (eg. in cases where unique_ptr is sufficient instead of shared_ptr).</li>
<li>Check pointers (for nullptr value) before use as necessary.</li>
</ul>

<h3>General</h3>
<ul>
<li>Use ranged-based loops as necessary:
<ul>
<li>for (auto x : vector) - use copies.</li>
<li>for (auto& x: vector) - modify/use original items.</li>
<li>for (auto const& x: vector) - not modify/use original items.</li>
</ul>
</li>
<li>Prefer pre-increment than post-increment.</li>
<li>Use typdef/alias as necessary.</li>
<li>Create reference variables as necessary (especially to reduce repetitive long lines when accessing something's member/function/etc).</li>
</ul>
