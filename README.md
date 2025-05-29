LINQ általános műveletek (C#):

1. Where - szűrés
   pl. var x = list.Where(x => x.Age > 18);

2. Select - leképezés
   pl. var x = list.Select(x => x.Name);

3. OrderBy / OrderByDescending - rendezés
   pl. var x = list.OrderBy(x => x.Name);
   pl. var x = list.OrderByDescending(x => x.Age);

4. ThenBy / ThenByDescending - másodlagos rendezés
   pl. var x= list.OrderBy(x => x.LastName).ThenBy(x => x.FirstName);

5. GroupBy - csoportosítás
   pl. var x = list.GroupBy(x => x.Category);

6. ToList / ToArray - listává/ tömbbé alakítás
   pl. var x = list.Where(x => x.Age > 18).ToList();

7. First / FirstOrDefault - első elem
   pl. var x= list.First(x => x.Name == "Anna");
   pl. var x = list.FirstOrDefault(x => x.Name == "Anna");

8. Single / SingleOrDefault - egyetlen elem (hibát dob, ha több van)
   pl. var x = list.Single(x => x.Id == 1);

9. Any - van-e ilyen elem
   pl. bool x = list.Any(x => x.Age > 18);

10. All - minden elemre igaz-e
    pl. bool x = list.All(x => x.Age > 18);

11. Count - elemszám
    pl. int x= list.Count(x => x.Age > 18);

12. Sum / Average / Min / Max - számolási műveletek
    pl. var x = list.Sum(x => x.Price);

13. Distinct - egyedi elemek
    pl. var x = list.Select(x => x.Name).Distinct();

14. Take / Skip - részhalmaz kivétele
    pl. var x = list.Take(5);
    pl. var x= list.Skip(2);

15. TakeWhile / SkipWhile - amíg igaz / amíg nem
    pl. var x= list.TakeWhile(x => x.Age < 30);

16. Reverse - megfordítás
    pl. var x = list.Reverse();

17. Join - belső összekapcsolás
    pl. var x= list1.Join(list2,
                                a => a.Id,
                                b => b.ForeignId,
                                (a, b) => new { a.Name, b.Value });

18. SelectMany - belső listák kibontása
    pl. var x = orders.SelectMany(x => x.Items);
