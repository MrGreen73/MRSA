# MRSA
The Program for Construction of Minimum Rectilinear Steiner Tree Using Genetic Algorithm.

   Описание алгоритма программы
Задача Штейнера состоит в том, чтобы соединить множество точек с использованием дополнительных вершин.
Все ребра в графе должны быть прямолинейными. 
Генетический алгоритм состоит из нескольких этапов:
1)	Генерация хромосом
2)	Скрещивание
3)	Мутация
4)	Селекция
5)	Оценка

Алгоритм, который использован для нахождения минимального прямолинейного дерева Штейнера(МПДШ) можно представить в виде псевдокода:
    generate(PC);
    evaluate(PC);
    repeat noOfGenerations times:
        PN  := ∅;
        repeat noOfOﬀspring times:
            select p1, p2 ∈ PC ;
            PN  := PN ∪ mutate(crossover(p1,p2)); 
        end;
        evaluate(PC ∪ PN);
        PC := select(PC ∪ PN); 
    end;
