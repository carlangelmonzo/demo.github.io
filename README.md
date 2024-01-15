# h1 Heading
## h2 Heading
### h3 Heading
#### h4 Heading
##### h5 Heading
###### h6 Heading


// This applies all the rules
// targeting the headings 
// placeholder class
h1, h2, h3,
h4, h5, h6 {
    @extend %headings !optional;
}

// Example use of headings 
// placeholder class
%headings {
    color: #2E2E2E;
    margin-bottom: 4px;
}

// Unstyles all anchor tags 
// inside a heading element
%headings > a {

    text-decoration: none;
    color: inherit;

    &:hover {
        text-decoration: underline;
    }

}

// Removes top margin of any p tag 
// that immediately follows a heading
%headings + p {
    margin-top: 0;
}

// Final Generated Output
// ======================

h1, h2, h3,
h4, h5, h6 {
    color: #2E2E2E;
    margin-bottom: 4px;
}

h1 > a, h2 > a, h3 > a,
h4 > a, h5 > a, h6 > a {
    text-decoration: none;
    color: inherit; 
}

h1 > a:hover, h2 > a:hover, h3 > a:hover,
h4 > a:hover, h5 > a:hover, h6 > a:hover {
    text-decoration: underline; 
}

h1 + p, h2 + p, h3 + p,
h4 + p, h5 + p, h6 + p {
    margin-top: 0; 
}
