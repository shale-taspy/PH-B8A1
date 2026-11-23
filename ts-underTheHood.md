Under the hood, tsc reads TypeScript source files, creates an Abstract Syntax Tree (AST), does type checking and symbol resolution on your code, and compiles it to JavaScript. During emit, TypeScript removes type annotations, interfaces, and type aliases while changing newer language features to meet your target context. Because type erasure occurs before runtime, TypeScript types are not present when JavaScript is executed.

The TypeScript compiler's main configuration file is tsconfig.json. It identifies the project root and controls how tsc handles files using compilerOptions. Settings like rootDir and outDir manage input and output directories, target and module govern emitted ECMAScript syntax and module systems, stringent impose severe type checking, and moduleDetection determines whether files are regarded as modules or scripts. Diagnostics identify type mismatches immediately away. By combining tsconfig.json and tsc, developers may standardize compilation rules throughout a codebase and identify errors before executing applications in browsers or Node.js during active development and testing.

//code example:
{
  "compilerOptions": {
    "rootDir": "./src",
    "outDir": "./dist",
    "module": "esnext",
    "target": "esnext",
    // Recommended Options
    "strict": true,
    "skipLibCheck": true,
    "moduleDetection": "force"
  }
}
