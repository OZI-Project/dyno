# OZI 1.0.4 meson.build:source_files,source_children
# Part of dyno.
# See LICENSE.txt in the project root for details.
# DO NOT EDIT BY HAND - This file was generated for use with OZI tools.
# ozi-fix -> meson rewrite is the standard editing pipeline.
source_files = ['ozi.phony', '__init__.py', 'py.typed']
foreach file: source_files
    if file != 'ozi.phony'
        fs.copyfile(file)
        if not meson.is_subproject() or get_option('install-subprojects').enabled()
            python.install_sources(file, subdir: 'dyno')
        endif
    endif
endforeach
ext_files = ['ozi.phony']
foreach file: ext_files
    if file != 'ozi.phony'
        if not meson.is_subproject() or get_option('install-subprojects').enabled()
            python.extension_module(
                fs.replace_suffix(file, ''),
                file,
                install: true,
                subdir: 'dyno',
                dependencies: python.dependency()
            )
        endif
    endif
endforeach
source_children = ['ozi.phony']
foreach child: source_children
    if child != 'ozi.phony'
        subdir(child)
    endif
endforeach
if false
    executable('source_files', source_files)
    executable('ext_files', ext_files)
    executable('source_children', source_children)
endif