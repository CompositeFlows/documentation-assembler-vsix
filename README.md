{
    "name": "documentation-assembler",
    "displayName": "Docs Assembler",
    "description": "Build documentation like Lego, using interchangeable blocks and fragments of text. A strategy for simplifying complex systems, that mirrors programming classes and variables.",
    "icon": "build-icons/_netOfTrees.icon-green-black-256.png",
    "version": "0.6.83",
    "publisher": "netoftrees",
    "preview": false,
    "private": true,
    "repository": {
        "type": "git",
        "url": "https://github.com/CompositeFlows/documentation-assembler-vsix"
    },
    "galleryBanner": {
        "color": "#232323",
        "theme": "dark"
    },
    "pricing": "Free",
    "engines": {
        "vscode": "^1.91.0"
    },
    "licence": "SEE LICENSE IN licence.txt",
    "categories": [
        "Other",
        "Education"
    ],
    "keywords": [
        "docs",
        "documentation",
        "GitHub Pages",
        "markdown",
        "guides",
        "help",
        "support",
        "knowledge",
        "trees",
        "manual"
    ],
    "main": "./out/extension.js",
    "activationEvents": [
        "workspaceContains:.bin/_context/"
    ],
    "homepage": "https://www.netoftrees.com",
    "contributes": {
        "customEditors": [
            {
                "viewType": "docsAssembler.cartographer",
                "displayName": "Cartographer",
                "selector": [
                    {
                        "filenamePattern": "*.tsmap"
                    }
                ],
                "priority": "default"
            },
            {
                "viewType": "docsAssembler.differentiator",
                "displayName": "Differentiator",
                "selector": [
                    {
                        "filenamePattern": "*.tsdif"
                    }
                ]
            },
            {
                "viewType": "docsAssembler.explorer",
                "displayName": "Explorer",
                "selector": [
                    {
                        "filenamePattern": "*.tsctx"
                    }
                ]
            }
        ],
        "configurationDefaults": {
            "workbench.editorAssociations": {
                "{git,gitlens,githistory}:file:/**/*.tsmap": "docsAssembler.cartographer"
            }
        },
        "viewsContainers": {
            "panel": [
                {
                    "id": "maps-compiler",
                    "title": "Map compiler",
                    "icon": "build-icons/_bots.svg"
                }
            ],
            "activitybar": [
                {
                    "id": "docs-assembler",
                    "title": "Docs Assembler",
                    "icon": "build-icons/tree.svg"
                }
            ]
        },
        "views": {
            "maps-compiler": [
                {
                    "type": "webview",
                    "id": "docsAssembler.compiler",
                    "name": "Docs Assembler reports",
                    "when": "docsAssembler.compiler.canShow"
                }
            ],
            "docs-assembler": [
                {
                    "type": "webview",
                    "id": "docsAssembler.control",
                    "name": "",
                    "contextualTitle": "Docs Assembler",
                    "when": "workspaceFolderCount > 0"
                }
            ]
        },
        "menus": {
            "webview/context": [
                {
                    "command": "docsAssembler.cartographer.openStepFile",
                    "when": "webviewId == 'docsAssembler.cartographer' && webviewSection == 'step'",
                    "group": "1_main@1"
                },
                {
                    "command": "docsAssembler.cartographer.insertStepAbove",
                    "when": "webviewId == 'docsAssembler.cartographer' && webviewSection == 'step'",
                    "group": "1_main@2"
                },
                {
                    "command": "docsAssembler.cartographer.sliceStep",
                    "when": "webviewId == 'docsAssembler.cartographer' && webviewSection == 'step'",
                    "group": "1_main@3"
                }
            ],
            "editor/title": [
                {
                    "command": "docsAssembler.cartographer.showJsonDiffEditor",
                    "group": "navigation",
                    "when": "resourceExtname == .tsmap && (activeEditor == workbench.editor.sidebysideEditor || isInDiffEditor == true)"
                }
            ],
            "view/title": [
                {
                    "command": "docsAssembler.compiler.clear",
                    "group": "navigation",
                    "when": "view == docsAssembler.compiler"
                },
                {
                    "command": "docsAssembler.compiler.collapse",
                    "group": "navigation",
                    "when": "view == docsAssembler.compiler"
                },
                {
                    "command": "docsAssembler.compiler.collapse.empty",
                    "group": "navigation",
                    "when": "view == docsAssembler.compiler && docsAssembler.compiler.reportView == 'compare'"
                }
            ],
            "explorer/context": [
                {
                    "command": "docsAssembler.explorer.createMap",
                    "group": "navigation",
                    "when": "docsAssembler.initialised && filesExplorerFocus && explorerResourceIsFolder"
                },
                {
                    "command": "docsAssembler.explorer.createStepFile",
                    "group": "navigation",
                    "when": "docsAssembler.initialised && filesExplorerFocus && explorerResourceIsFolder"
                },
                {
                    "command": "docsAssembler.explorer.createVariablesFile",
                    "group": "navigation",
                    "when": "docsAssembler.initialised && filesExplorerFocus && explorerResourceIsFolder"
                }
            ]
        },
        "languages": [
            {
                "id": "tsmap",
                "aliases": [
                    "tsmap",
                    "TSMAP",
                    "TsMap"
                ],
                "extensions": [
                    ".tsmap"
                ],
                "icon": {
                    "light": "./build-icons/tsmapFileIcon.svg",
                    "dark": "./build-icons/tsmapFileIcon.svg"
                },
                "configuration": "./language-configuration.json"
            },
            {
                "id": "tsctx",
                "aliases": [
                    "tsctx"
                ],
                "extensions": [
                    ".tsctx"
                ],
                "icon": {
                    "light": "./build-icons/trees-bluey.svg",
                    "dark": "./build-icons/trees-bluey.svg"
                },
                "configuration": "./language-configuration.json"
            },
            {
                "id": "tscom",
                "aliases": [
                    "tscom"
                ],
                "extensions": [
                    ".tscom"
                ],
                "icon": {
                    "light": "./build-icons/cog.svg",
                    "dark": "./build-icons/cog.svg"
                },
                "configuration": "./language-configuration.json"
            },
            {
                "id": "markdown",
                "aliases": [
                    "tsstp",
                    "tsvar",
                    "tsfrg"
                ],
                "extensions": [
                    ".tsstp",
                    ".tsvar",
                    ".tsfrg"
                ]
            }
        ],
        "grammars": [
            {
                "scopeName": "docAssembler.markdown",
                "path": "./syntaxes/docAssembler.markdown.json",
                "injectTo": [
                    "text.html.markdown"
                ]
            },
            {
                "scopeName": "docAssembler.markdownLink",
                "path": "./syntaxes/docAssemblerLink.markdownLink.json",
                "injectTo": [
                    "meta.link.inline.markdown"
                ]
            }
        ],
        "commands": [
            {
                "command": "docsAssembler.explorer.createMap",
                "title": "New map...",
                "category": "explorer",
                "icon": "./build-icons/createMapCodicon.svg"
            },
            {
                "command": "docsAssembler.explorer.createStepFile",
                "title": "New step file...",
                "category": "explorer",
                "icon": "./build-icons/createAssetCodicon.svg"
            },
            {
                "command": "docsAssembler.explorer.createVariablesFile",
                "title": "New variables file...",
                "category": "explorer",
                "icon": "./build-icons/createVariableCodicon.svg"
            },
            {
                "command": "docsAssembler.compiler.clear",
                "category": "compiler",
                "title": "Clear",
                "icon": "$(clear-all)"
            },
            {
                "command": "docsAssembler.compiler.collapse",
                "category": "compiler",
                "title": "Collapse",
                "icon": "$(collapse-all)"
            },
            {
                "command": "docsAssembler.compiler.collapse.empty",
                "category": "compiler",
                "title": "Collapse empty pub folders",
                "icon": "./build-icons/collapseEmptyCodicon.svg"
            },
            {
                "command": "docsAssembler.compiler.canShow",
                "title": "compiler.canShow",
                "category": "compiler"
            },
            {
                "command": "docsAssembler.compiler.reportView",
                "title": "compiler.reportView",
                "category": "compiler"
            },
            {
                "command": "docsAssembler.initialised",
                "title": "initialised",
                "category": "assembler"
            },
            {
                "command": "docsAssembler.cartographer.insertStepAbove",
                "title": "Insert step above",
                "category": "cartographer"
            },
            {
                "command": "docsAssembler.cartographer.sliceStep",
                "title": "Splice step out",
                "category": "cartographer"
            },
            {
                "command": "docsAssembler.cartographer.openStepFile",
                "title": "Open step in markdown editor",
                "category": "cartographer"
            },
            {
                "command": "docsAssembler.cartographer.showJsonDiffEditor",
                "title": "Show json diff editor",
                "category": "cartographer",
                "icon": "./build-icons/diff.svg"
            },
            {
                "command": "docsAssembler.cartographer.upArrow",
                "title": "cartographer.upArrow",
                "category": "cartographer"
            },
            {
                "command": "docsAssembler.cartographer.shiftAndUpArrow",
                "title": "cartographer.shiftAndUpArrow",
                "category": "cartographer"
            },
            {
                "command": "docsAssembler.cartographer.downArrow",
                "title": "cartographer.downArrow",
                "category": "cartographer"
            },
            {
                "command": "docsAssembler.cartographer.shiftAndDownArrow",
                "title": "cartographer.shiftAndDownArrow",
                "category": "cartographer"
            },
            {
                "command": "docsAssembler.cartographer.pageUp",
                "title": "cartographer.pageUp",
                "category": "cartographer"
            },
            {
                "command": "docsAssembler.cartographer.pageDown",
                "title": "cartographer.pageDown",
                "category": "cartographer"
            },
            {
                "command": "docsAssembler.cartographer.home",
                "title": "cartographer.home",
                "category": "cartographer"
            },
            {
                "command": "docsAssembler.cartographer.end",
                "title": "cartographer.end",
                "category": "cartographer"
            },
            {
                "command": "docsAssembler.cartographer.rightArrow",
                "title": "cartographer.rightArrow",
                "category": "cartographer"
            },
            {
                "command": "docsAssembler.cartographer.lens.update",
                "title": "cartographer.lens.update",
                "category": "cartographer.lens"
            },
            {
                "command": "docsAssembler.cartographer.lens.delete",
                "title": "cartographer.lens.delete",
                "category": "cartographer.lens"
            },
            {
                "command": "docsAssembler.cartographer.lens.cancel",
                "title": "cartographer.lens.cancel",
                "category": "cartographer.lens"
            }
        ],
        "keybindings": [
            {
                "command": "docsAssembler.cartographer.upArrow",
                "key": "up",
                "when": "resourceExtname == .tsmap"
            },
            {
                "command": "docsAssembler.cartographer.shiftAndUpArrow",
                "key": "shift+up",
                "when": "resourceExtname == .tsmap"
            },
            {
                "command": "docsAssembler.cartographer.downArrow",
                "key": "down",
                "when": "resourceExtname == .tsmap"
            },
            {
                "command": "docsAssembler.cartographer.shiftAndDownArrow",
                "key": "shift+down",
                "when": "resourceExtname == .tsmap"
            },
            {
                "command": "docsAssembler.cartographer.pageUp",
                "key": "pageup",
                "when": "resourceExtname == .tsmap"
            },
            {
                "command": "docsAssembler.cartographer.pageDown",
                "key": "pagedown",
                "when": "resourceExtname == .tsmap"
            },
            {
                "command": "docsAssembler.cartographer.home",
                "key": "home",
                "when": "resourceExtname == .tsmap"
            },
            {
                "command": "docsAssembler.cartographer.end",
                "key": "end",
                "when": "resourceExtname == .tsmap"
            },
            {
                "command": "docsAssembler.cartographer.rightArrow",
                "key": "right",
                "when": "resourceExtname == .tsmap"
            },
            {
                "command": "docsAssembler.cartographer.lens.update",
                "key": "shift+alt+l shift+alt+u",
                "when": "resourceExtname == .tsmap"
            },
            {
                "command": "docsAssembler.cartographer.lens.delete",
                "key": "shift+alt+l shift+alt+d",
                "when": "resourceExtname == .tsmap"
            },
            {
                "command": "docsAssembler.cartographer.lens.cancel",
                "key": "shift+alt+l shift+alt+c",
                "when": "resourceExtname == .tsmap"
            }
        ],
        "configuration": {
            "title": "Docs Assembler",
            "properties": {
                "editor.tokenColorCustomizations.textMateRules": {
                    "type": "array",
                    "description": "Token colours."
                },
                "docsAssembler.helpText.show": {
                    "type": "boolean",
                    "default": true,
                    "description": "Show inline help text in the lens.",
                    "order": 7
                },
                "docsAssembler.map.option.defaultSingleText": {
                    "type": "string",
                    "default": "Next",
                    "description": "Default option text where there is a single option.",
                    "order": 6
                },
                "docsAssembler.map.asset.folder": {
                    "type": "string",
                    "default": "δ steps",
                    "description": "Folder name for a tsmap's assets. It will be located in the same directory as the tsmap.",
                    "order": 3
                },
                "docsAssembler.publish.folder": {
                    "type": "string",
                    "default": "pub",
                    "description": "Folder name for published files.",
                    "order": 1
                },
                "docsAssembler.docs.folder": {
                    "type": "string",
                    "default": "docs",
                    "description": "Folder name for docs.",
                    "order": 2
                },
                "docsAssembler.docs.deleteExclude": {
                    "type": "array",
                    "default": [],
                    "description": "Which files are excluded when the contents of the docs folder is cleared.",
                    "order": 5
                },
                "docsAssembler.tsmaps.folder": {
                    "type": "string",
                    "default": "tsmaps",
                    "description": "Folder name for docs.",
                    "order": 0
                },
                "docsAssembler.map.variable.folder": {
                    "type": "string",
                    "default": "Ω variables",
                    "description": "Folder name for a tsmap's variableFiles. It will be located in the same directory as the tsmap.",
                    "order": 4
                }
            }
        },
        "jsonValidation": [
            {
                "fileMatch": "**/*.tsmap",
                "url": "./tzrschema.json"
            }
        ]
    },
    "scripts": {
        "e-dev": "cd uis/explorerView && npm run dev",
        "e-build": "cd uis/explorerView && npm run build",
        "e-min-build": "cd uis/explorerView && npx vite build --config vite-min.config.js",
        "e-update": "cd uis/explorerView && npm update",
        "e-ck": "cd uis/explorerView && tsc --noEmit",
        "e-lint": "cd uis/explorerView && eslint",
        "c-dev": "cd uis/cartographerView && npm run dev",
        "c-build": "cd uis/cartographerView && npm run build",
        "c-min-build": "cd uis/cartographerView && npx vite build --config vite-min.config.js",
        "c-update": "cd uis/cartographerView && npm update",
        "c-ck": "cd uis/cartographerView && tsc --noEmit",
        "c-lint": "cd uis/cartographerView && eslint",
        "m-dev": "cd uis/monacoEditor && npm run dev",
        "m-build": "cd uis/monacoEditor && npm run build",
        "m-min-build": "cd uis/monacoEditor && npx vite build --config vite-min.config.js",
        "m-update": "cd uis/monacoEditor && npm update",
        "m-ck": "cd uis/monacoEditor && tsc --noEmit",
        "m-lint": "cd uis/monacoEditor && eslint src --ext ts",
        "d-dev": "cd uis/differentiatorView && npm run dev",
        "d-build": "cd uis/differentiatorView && npm run build",
        "d-min-build": "cd uis/differentiatorView && npx vite build --config vite-min.config.js",
        "d-update": "cd uis/differentiatorView && npm update",
        "d-ck": "cd uis/differentiatorView && tsc --noEmit",
        "d-lint": "cd uis/differentiatorView && eslint src --ext ts",
        "g-dev": "cd uis/controlView && npm run dev",
        "g-build": "cd uis/controlView && npm run build",
        "g-min-build": "cd uis/controlView && npx vite build --config vite-min.config.js",
        "g-update": "cd uis/controlView && npm update",
        "g-ck": "cd uis/controlView && tsc --noEmit",
        "g-lint": "cd uis/controlView && eslint src --ext ts",
        "a-dev": "cd uis/compilerView && npm run dev",
        "a-build": "cd uis/compilerView && npm run build",
        "a-min-build": "cd uis/compilerView && npx vite build --config vite-min.config.js",
        "a-update": "cd uis/compilerView && npm update",
        "a-ck": "cd uis/compilerView && tsc --noEmit",
        "a-lint": "cd uis/compilerView && eslint src --ext ts",
        "partial-web-build": "yarn a-build && yarn c-build && yarn e-build && yarn g-build && yarn d-build",
        "web-build": "yarn a-build && yarn c-build && yarn e-build && yarn g-build && yarn d-build && yarn m-build",
        "min-web-build": "yarn a-min-build && yarn c-min-build && yarn e-min-build && yarn g-min-build && yarn d-min-build && yarn m-min-build",
        "vscode:prepublish": "npm run compile",
        "compile": "tsc -p ./",
        "watch": "tsc -watch -p ./",
        "pretest": "npm run compile && npm run lint",
        "ck": "tsc --noEmit",
        "lint": "eslint src --ext ts"
    },
    "devDependencies": {
        "@types/js-yaml": "^4.0.9",
        "@types/node": "^16.18.70",
        "@types/vscode": "^1.74.0",
        "@types/vscode-webview": "^1.57.0",
        "@typescript-eslint/eslint-plugin": "^5.42.0",
        "@typescript-eslint/parser": "^5.42.0",
        "esbuild": "^0.25.2",
        "eslint": "^8.26.0",
        "prettier": "^2.8.1",
        "vscode-test": "^1.5.0"
    },
    "dependencies": {
        "js-yaml": "^4.1.0",
        "json5": "^2.2.3"
    }
}
