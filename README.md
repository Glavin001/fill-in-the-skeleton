# fill-in-the-skeleton
Skeleton of Thought meets Fill-in-the-Middle (FIM) training

Read https://arxiv.org/abs/2307.15337 and https://arxiv.org/abs/2207.14255

Example for code generation:

```html
<|start_skeleton|>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Multi-Column Nested Layout</title>
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
</head>
<body class="bg-gray-100">

    <!-- Main flex container -->
    <div class="flex h-screen">

        <!-- Sidebar -->
        <div class="bg-gray-800 text-white w-64 p-5">
<|fill_start|>1<|fill_end|>
        </div>

        <!-- Content area -->
        <div class="flex-1 flex flex-col">
<|fill_start|>2<|fill_end|>
        </div>
    </div>

</body>
</html>
<|end_skeleton|>
<|start_skeleton|>1
            <h1 class="text-xl font-semibold mb-5">Sidebar</h1>
            <ul>
                <li class="mb-3">Home</li>
                <li class="mb-3">About</li>
                <li class="mb-3">Services</li>
                <li>Contact</li>
            </ul>
<|end_skeleton|>
<|start_skeleton|>2
            <!-- Top navigation bar -->
            <div class="bg-gray-700 text-white p-5">
                <h2 class="text-lg font-semibold">Top Navigation</h2>
            </div>

            <!-- Body content -->
            <div class="flex-1 p-10">
                <h3 class="text-2xl font-semibold mb-5">Main Body Content</h3>
                <p>
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed non risus. Suspendisse lectus tortor, dignissim sit amet, adipiscing nec, ultricies sed, dolor. Cras elementum ultrices diam.
                </p>
            </div>
<|end_skeleton|>
<|EOS|>
```
