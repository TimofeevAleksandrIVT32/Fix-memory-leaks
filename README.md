# Fix memory leaks

Поиск с помощью valgrind утечек памяти и их исправление.

## Файл package-install 
## До:

==14337== 
==14337== HEAP SUMMARY:
==14337==     in use at exit: 2,077,967 bytes in 32,810 blocks
==14337==   total heap usage: 110,106 allocs, 77,296 frees, 35,734,793 bytes allocated
==14337== 
==14337== LEAK SUMMARY:
==14337==    definitely lost: 2,490 bytes in 149 blocks
==14337==    indirectly lost: 990 bytes in 66 blocks
==14337==      possibly lost: 2,032,683 bytes in 32,583 blocks
==14337==    still reachable: 41,804 bytes in 12 blocks
==14337==         suppressed: 0 bytes in 0 blocks
==14337== Rerun with --leak-check=full to see details of leaked memory
==14337== 
==14337== For lists of detected and suppressed errors, rerun with: -s
==14337== ERROR SUMMARY: 0 errors from 0 contexts (suppressed: 0 from 0)

## После:

==15194== 
==15194== HEAP SUMMARY:
==15194==     in use at exit: 0 bytes in 0 blocks
==15194==   total heap usage: 138,776 allocs, 138,776 frees, 38,400,617 bytes allocated
==15194== 
==15194== All heap blocks were freed -- no leaks are possible
==15194== 
==15194== For lists of detected and suppressed errors, rerun with: -s
==15194== ERROR SUMMARY: 0 errors from 0 contexts (suppressed: 0 from 0)

## Файл package-install-dependencies
## До:

==14433== 
==14433== HEAP SUMMARY:
==14433==     in use at exit: 1,399,201 bytes in 21,863 blocks
==14433==   total heap usage: 73,961 allocs, 52,098 frees, 21,177,358 bytes allocated
==14433== 
==14433== LEAK SUMMARY:
==14433==    definitely lost: 1,615 bytes in 85 blocks
==14433==    indirectly lost: 660 bytes in 44 blocks
==14433==      possibly lost: 1,355,122 bytes in 21,722 blocks
==14433==    still reachable: 41,804 bytes in 12 blocks
==14433==         suppressed: 0 bytes in 0 blocks
==14433== Rerun with --leak-check=full to see details of leaked memory
==14433== 
==14433== For lists of detected and suppressed errors, rerun with: -s
==14433== ERROR SUMMARY: 0 errors from 0 contexts (suppressed: 0 from 0)

## После:

==15292== 
==15292== HEAP SUMMARY:
==15292==     in use at exit: 0 bytes in 0 blocks
==15292==   total heap usage: 73,937 allocs, 73,937 frees, 21,177,534 bytes allocated
==15292== 
==15292== All heap blocks were freed -- no leaks are possible
==15292== 
==15292== For lists of detected and suppressed errors, rerun with: -s
==15292== ERROR SUMMARY: 0 errors from 0 contexts (suppressed: 0 from 0)

## Файл package-install-dev-dependencies
## До:

==14492== 
==14492== HEAP SUMMARY:
==14492==     in use at exit: 1,397,416 bytes in 21,759 blocks
==14492==   total heap usage: 66,257 allocs, 44,498 frees, 9,154,523 bytes allocated
==14492== 
==14492== LEAK SUMMARY:
==14492==    definitely lost: 340 bytes in 15 blocks
==14492==    indirectly lost: 150 bytes in 10 blocks
==14492==      possibly lost: 1,355,122 bytes in 21,722 blocks
==14492==    still reachable: 41,804 bytes in 12 blocks
==14492==         suppressed: 0 bytes in 0 blocks
==14492== Rerun with --leak-check=full to see details of leaked memory
==14492== 
==14492== For lists of detected and suppressed errors, rerun with: -s
==14492== ERROR SUMMARY: 0 errors from 0 contexts (suppressed: 0 from 0)

## После:

==15350== 
==15350== HEAP SUMMARY:
==15350==     in use at exit: 0 bytes in 0 blocks
==15350==   total heap usage: 66,259 allocs, 66,259 frees, 9,154,775 bytes allocated
==15350== 
==15350== All heap blocks were freed -- no leaks are possible
==15350== 
==15350== For lists of detected and suppressed errors, rerun with: -s
==15350== ERROR SUMMARY: 0 errors from 0 contexts (suppressed: 0 from 0)

## Файл package-new-from-slug
## До:

==14526== 
==14526== HEAP SUMMARY:
==14526==     in use at exit: 719,929 bytes in 10,897 blocks
==14526==   total heap usage: 37,056 allocs, 26,159 frees, 5,595,739 bytes allocated
==14526== 
==14526== LEAK SUMMARY:
==14526==    definitely lost: 384 bytes in 12 blocks
==14526==    indirectly lost: 180 bytes in 12 blocks
==14526==      possibly lost: 677,561 bytes in 10,861 blocks
==14526==    still reachable: 41,804 bytes in 12 blocks
==14526==         suppressed: 0 bytes in 0 blocks
==14526== Rerun with --leak-check=full to see details of leaked memory
==14526== 
==14526== For lists of detected and suppressed errors, rerun with: -s
==14526== ERROR SUMMARY: 0 errors from 0 contexts (suppressed: 0 from 0)

## После:

==15385== 
==15385== HEAP SUMMARY:
==15385==     in use at exit: 0 bytes in 0 blocks
==15385==   total heap usage: 37,060 allocs, 37,060 frees, 5,595,891 bytes allocated
==15385== 
==15385== All heap blocks were freed -- no leaks are possible
==15385== 
==15385== For lists of detected and suppressed errors, rerun with: -s
==15385== ERROR SUMMARY: 0 errors from 0 contexts (suppressed: 0 from 0)
