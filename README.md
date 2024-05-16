// morgan.codes vscode theme example
return (
<Layout>
div className="doc-container"
<h3 className="doc-container-header">Google Docs</h3>
{data.hits.map(item ⇒ (
<Doc
))}
</div>
header={item.title}
body={item.points}
<div className="zettel-container">
<h3 className="zettel-container-header">Zettels</h3>
{data.hits.map(item ⇒ (
<Notecard
title={(item.title).substr(0, 28) + '... '}
description={item.author}
tags={item._tags}
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
43
44
45
);
46
}
))}
</div>
<<< Layout>
47
48
export default Dashboard